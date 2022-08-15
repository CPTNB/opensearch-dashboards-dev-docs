# Hello World Plugin!

In this tutorial doc I'm going to walk you through basic plugin creation and adding simple features to the plugin. In the end from our sample plugin, we will be able to make API calls to OpenSearch and fetch index documents along with showing the documents data in the timeseries graph using elastic charts. 

First we are going to see how to generate a simple plugin within the OSD repo. 

For this we are using [@osd/plugin-generator](https://github.com/opensearch-project/OpenSearch-Dashboards/tree/1.2/src/plugins) package which scaffolds a plugin template for us.

### Step 1: Run the below command in the OSD package root terminal

```ts
node scripts/generate_plugin --name my_example_plugin -y // generates a plugin in `example/my_example_plugin`
```
Once you run the above command, plugin generator will ask you few questions on where you would like your plugin folder to be created, if you are interested in creating server side plugin or client side plugin or both. Once you answer those questions, your sample plugin intial setup will be bootstrapped and generated in the desired folder path within OSD. 

For this tutorial, I've generated an example plugin with both public and server side contracts. 

The generate script supports a few flags; run it with the --help flag to learn more.

```ts
node scripts/generate_plugin --help
```

### Step 2 : Add dependency on `Data` plugin in the `opensearch_dashboards.json` manifest file

```json
{
  "id": "myExamplePlugin",
  "version": "1.0.0",
  "opensearchDashboardsVersion": "opensearchDashboards",
  "server": true,
  "ui": true,
  "requiredPlugins": ["developerExamples", "data"],
  "optionalPlugins": []
}
```
The manifest file signature is defined by the interface [PluginManifest](https://github.com/opensearch-project/OpenSearch-Dashboards/blob/1.2/src/core/server/plugins/types.ts#L126-L196)

### Step 3: Add a new  interface property of type `DataPublicPluginStart` in the `AppPluginStartDependencies` interface defined in the `types.ts` file in the public folder

Note that we are importing `DataPublicPluginStart` interface from `data` plugin's public `types` as we are making use of it in our client side plugin. 

### Step 4 : In `../public/plugin.ts` file, inside the `setup` method, we are getting all the start services dependencies as specified in the `opensearch_dashboards.json` through `core.getStartServices()` and render the application with all the dependencies already mounted. 

```ts
public setup(
    core: CoreSetup)  {
    // Register an application into the side navigation menu
    core.application.register({
      id: 'myExamplePlugin',
      title: PLUGIN_NAME,
      async mount(params: AppMountParameters) {
        // Load application bundle
        const { renderApp } = await import('./application');
        // Get start services as specified in opensearch_dashboards.json
        const [coreStart, depsStart] = await core.getStartServices();
        // Render the application
        return renderApp(coreStart, depsStart as AppPluginStartDependencies, params);
      },
    });

    // Return methods that should be available to other plugins
    return {
      getGreeting() {},
    };
}
```
Note that to share contracts between plugins is when we return something from the lifecycle methods of plugin, that is how other plugins can consume and depend on it. In the above example, method `getGreeting()` will be available for other plugins to consumer. 

```ts
// Return methods that should be available to other plugins
    return {
      getGreeting() {
        return i18n.translate('myExamplePlugin.greetingText', {
          defaultMessage: 'Hello from {name}!',
          values: {
            name: PLUGIN_NAME,
          },
        });
      },
    };
```

### Step 5: Now that we have introduced `data` plugin as plugin start dependency to render our app, in the `../plugins/application.tsx` file we need to inject the new binding variable `data` to the `<MyExamplePluginApp>` UI component which renders the plugin landing page. 

```tsx
export const renderApp = (
  { http }: CoreStart,
  { data }: AppPluginStartDependencies,
  { appBasePath, element }: AppMountParameters
) => {
  ReactDOM.render(
    <MyExamplePluginApp
      basename={appBasePath}
      http={http}
      data={data}
    />,
    element
  );

  return () => ReactDOM.unmountComponentAtNode(element);
};
```
### Step 6: Let's add a simple button which on click will make a backend call to `data` plugin's search API `/search/opensearch` and fetch the documents.

```tsx
<EuiButton type="primary" size="s" onClick={onSearchHandler}>
  <FormattedMessage id="myExamplePlugin.buttonText"      defaultMessage="Search Data" />
</EuiButton>

<pre>
  {JSON.stringify(hits, null, 2)}
</pre>
```

### step 7: Add a handler to trigger API calls to the high-level data plugin's services

```tsx
const [hits, setHits] = useState<Array<Record<string, any>>>();

const onSearchHandler = async () => {
    const searchSource = await data.search.searchSource.create();
    const defaultIndexPattern = await data.indexPatterns.getDefault();
    const searchResponse = await searchSource
     .setField('index', defaultIndexPattern)
     .setField('size', 100)
     .fetch();

    setHits(searchResponse.hits.hits);
    
};
```
`Data` plugin's `search` service provides access to OpenSearch using the high-level `SearchSource` API. Note that we are aso using `IndexPatterns`  contract to get the default index pattern and use it to set the `index` field on the `searchSource` request payload. This is required field on the request payload, as Index `title` field will be required to search the documents from specific index pattern. 

### Step 8: Once the index documents are fetched on click of `Search Data` button, we can now show the data in one of the timeseries graph using Charts. 

```tsx
import { BarSeries, Chart, Axis } from '@elastic/charts';
```
Embed the below component in the `app.tsx` to generate the bar graph representing fields in the index documents. 

```tsx
<div>
    {hits &&
    <Chart size={{height: 200}}>
      <BarSeries 
        id="myExamplePlugin"
        name="myExamplePlugin"
        data={[0,1],[1,2]}
        xScaleType="time"
        xAccessor={0}
        yAccessors={[1]}
      />
      <Axis
        id="bottom-axis"
        position="bottom"
      />
      <Axis
        id="left-axis"
        position="left"
      />
    </Chart>
    }
  </div>

```
You can modify the `data` property on `BarSeries` component to feed the appropriate index property fields from your document. 


### Step 9: As a last step, we can register the sample plugin inside developer example plugin.

* Add `developerExamples` as a required Plugin dependency in the manifest json file.

```
 "requiredPlugins": ["developerExamples", "data"],
```

Inside `../public/plugin.ts` file, `Setup` method, register the demo plugin. 

```tsx
import { DeveloperExamplesSetup } from '../../developer_examples/public';

interface SetupDeps {
  developerExamples: DeveloperExamplesSetup;
}

public setup(
    core: CoreSetup, { developerExamples }: SetupDeps)  {

      developerExamples.register({
      title: PLUGIN_NAME,
      description: `This is a sample plugin making backend API call to Opensearch and represent the data in timeseries graph.`,
      appId: 'myExamplePlugin',
    });

    return {}
}
```
