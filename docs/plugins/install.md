# Install your plugin

## From source
If you are doing development on your external plugin, `cd` into `{root}/plugins` and add your plugin there.

## From bin
This section is if you have access to `bin/opensearch-dashboards-plugin` which you should only be using if you have a build of OpenSearch Dashboards.

### From URL
If have you have an URL of a zip of your plugin, you can install your plugin with:
```
./opensearch-dashboards-plugin install <plugin-url.zip>
```

### From ID
If you know that this plugin is built from the OpenSearch-Project, you can install your plugin with:
```
# Note the camelCase
./opensearch-dashboards-plugin install <pluginId>
```

### From file
If you have a local zip of the plugin, you can install your plugin with:
```
./opensearch-dashboards-plugin install <path-to-plugin.zip>
```