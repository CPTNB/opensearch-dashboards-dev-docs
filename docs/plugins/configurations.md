# Configure your plugin

### Hide plugins
Most plugins come with `enabled` defined in their config. Check the `opensearch_dashboards.json` file for the `id` property or if preset `configPath`. Then in `{root}/config/opensearch_dashboards.yml` set `enabled` to `false`. If no value is set, then the application will assume it is enabled.

For example, to hide the Discover plugin:
```
discover.enabled: false
```