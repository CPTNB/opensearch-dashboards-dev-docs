# Setup and Run i18n-plugin

i18n-plugin needs to run on OpenSearch Dashboards. Therefore, we also need to setup for OpenSearch and OpenSearch Dashboards. 

## Environment Setup

1. Download OpenSearch. You could clone the [OpenSearch repo](https://github.com/opensearch-project/OpenSearch.git), use [docker](https://opensearch.org/docs/latest/opensearch/install/docker/) or [artifact](https://opensearch.org/docs/latest/opensearch/install/tar/). Make sure the version matches the OpenSearch Dashboards version.
2. Setup the environment to run OpenSearch Dashboards. You will need to install [node.js](https://nodejs.org/en/), [nvm](https://github.com/nvm-sh/nvm/blob/master/README.md), and [yarn](https://yarnpkg.com/) in your environment to properly pull down dependencies to build and bootstrap.
3. Download the OpenSearch-Dashboards source code.

   See the [OpenSearch Dashboards developer guide](https://github.com/opensearch-project/OpenSearch/blob/main/DEVELOPER_GUIDE.md) for more instructions on setting up your development environment.

4. Change your node version to the version specified in `.node-version` inside the OpenSearch-Dashboards root directory.
5. cd into the `plugins` directory of the OpenSearch-Dashboards source code directory. Clone [i18n-plugin](https://github.com/opensearch-project/i18n-plugin.git) into the `plugins` directory. Ultimately, your directory structure should look like this:

```md
.
├── OpenSearch-Dashboards
│   └── plugins
│       └── i18n-plugin
```
6. Config localization in i18n-plugin. Add a locale json file in `translations` directory of the i18n-plugin. Specify the path in `.i18nrc.json`. For example, if the locale json file you added is called `zh-CN.json`, the path should be `"translations": ["translations/zh-CN.json"`.
7. Config localization in OpenSearch Dashboards. cd into the `config` directory of the OpenSearch-Dashboards source code directory. Add `i18n.locale: "{your locale}"` in `opensearch_dashboards.yml` file.
8. Run `yarn osd bootstrap` under `Opensearch-Dashboards`.

## Run

- `yarn start`

  - Starts OpenSearch-Dashboards and includes this plugin. A localized OpenSearch-Dashboards will be available on `localhost:5601`.
  - Please run in the OpenSearch-Dashboards root directory
  - You must have OpenSearch running.