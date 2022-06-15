# Build your plugin

To build a zip of your plugin, run the following:
```
yarn plugin-helpers build
```
This will produce a zip file under `{root}/plugins/{plugin}/build/{plugin-id}-{plugin-version}.zip`

If you would like to build a zip of your plugin for a specific version of OpenSearch Dashboards, run the following:
```
yarn plugin-helpers build --opensearch-dashboards-version={desired-version}
```
This will produce a zip file under `{root}/plugins/{plugin}/build/{plugin-id}-{desired-version}.zip`. The benefit here is that this will set the `opensearchDashboardsVersion` in `{plugin}/opensearch_dashboards.json` to be `{desired-version}`. So even if the plugin version does not match OpenSearch Dashboards will check if `opensearchDashboardsVersion` is the current version of OpenSearch Dashboards.