# Configure enable/disable plugin using config yaml file

## How to add new config to the `{root}/config/opensearch-dashboards.yml` file?

### 1. Add a commented out new config value in the `opensearch_dashboards.yml` file. Below is an example where I'm adding new flag to hide/show
`wizard` plugin.

```yml

# Set the value of this setting to true to start exploring wizard
# functionality in Visualization.
# wizard.enabled: true
```

Note that the yml config values are read as path to the plugin config schema file. In the above example, `wizard` is the `Id` of the plugin to which I'm introducing this new config value. The value should match the default, so that if a user uncomments the line, it will still have the default behavior.


### 2. Create a new config schema for the plugin. We should have this config file defined in the root folder of the plugin. For example, `config.ts` for `wizard` plugin is defined in the `src/plugin/wizard/config.ts`

```ts

import { schema, TypeOf } from '@osd/config-schema';

export const configSchema = schema.object({
  enabled: schema.boolean({ defaultValue: true }),
});

export type ConfigSchema = TypeOf<typeof configSchema>;
```
Every plugin by default has `enabled` true if not defined in the config schema. When defined in the config schema, the value for if plugin should be enabled is read from here. This config value is overriden, when we define the config value in `opensearch_dashboards.yml`.

### 3. Export the new config schema in the `index.ts` file of the plugin's server folder. This is required for plugin to read the properties to expose to client during plugin registration. 

```ts
export const config: PluginConfigDescriptor<ConfigSchema> = {
  exposeToBrowser: {
    enabled: true,
  },
  schema: configSchema,
};

```
We need to set `exposeToBrowser` true for the config property `enabled` which we have defined in the config schema. `exposeToBrowser` will allow the components in the `public` folder to get the value of the config but is still usable in the `server` components even without this setting.

### 4. Now we can use the config schema in the `plugin.ts` class constructor, inside `public` folder of the plugin.

```ts
import { ConfigSchema } from '../config';

constructor(public initializerContext PluginInitializerContext<ConfigSchema>) {}
```