<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [DiscoveredPlugin](./opensearch-dashboards.discoveredplugin.md) &gt; [requiredBundles](./opensearch-dashboards.discoveredplugin.requiredbundles.md)

## DiscoveredPlugin.requiredBundles property

List of plugin ids that this plugin's UI code imports modules from that are not in `requiredPlugins`<!-- -->.

<b>Signature:</b>

```typescript
readonly requiredBundles: readonly PluginName[];
```

## Remarks

The plugins listed here will be loaded in the browser, even if the plugin is disabled. Required by `@osd/optimizer` to support cross-plugin imports. "core" and plugins already listed in `requiredPlugins` do not need to be duplicated here.

