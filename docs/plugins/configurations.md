# Configure your plugin

### Configuration file
You can configure your plugin by setting values in `{root}/config/opensearch_dashboards.yml`.

For example:
```
server.maxPayloadBytes: 1759977
```

### Configure by argument
You can configure your plugin by passing arguments in your start up command.

For example, when starting the application in local development:
```
yarn start --server.maxPayloadBytes=1759977
```

For example, when starting the application via the executable:
```
./bin/opensearch-dashboards --server.maxPayloadBytes=1759977
```

### Configure the data source
When doing local development, you can configure your data source (OpenSearch) via the CLI.

For example, when running the data source via snapshot:
```
yarn opensearch snapshot -E cluster.name=test
```

This will start up an OpenSearch snapshot that matches the current version of your OpenSearch Dashboards set in `{root}/package.json`. Then configure OpenSearch cluster name to be `test`.

### Hide plugins
Most plugins come with `enabled` defined in their config. Check the `opensearch_dashboards.json` file for the `id` property or if preset `configPath`. Then in `{root}/config/opensearch_dashboards.yml` set `enabled` to `false`. If no value is set, then the application will assume it is enabled.

For example, to hide the Discover plugin:
```
discover.enabled: false
```