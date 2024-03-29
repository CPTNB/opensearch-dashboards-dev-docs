<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [DiscoveredPlugin](./opensearch-dashboards.discoveredplugin.md)

## DiscoveredPlugin interface

Small container object used to expose information about discovered plugins that may or may not have been started.

<b>Signature:</b>

```typescript
export interface DiscoveredPlugin 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [configPath](./opensearch-dashboards.discoveredplugin.configpath.md) | ConfigPath | Root configuration path used by the plugin, defaults to "id" in snake\_case format. |
|  [id](./opensearch-dashboards.discoveredplugin.id.md) | [PluginName](./opensearch-dashboards.pluginname.md) | Identifier of the plugin. |
|  [optionalPlugins](./opensearch-dashboards.discoveredplugin.optionalplugins.md) | readonly [PluginName](./opensearch-dashboards.pluginname.md)<!-- -->\[\] | An optional list of the other plugins that if installed and enabled \*\*may be\*\* leveraged by this plugin for some additional functionality but otherwise are not required for this plugin to work properly. |
|  [requiredBundles](./opensearch-dashboards.discoveredplugin.requiredbundles.md) | readonly [PluginName](./opensearch-dashboards.pluginname.md)<!-- -->\[\] | List of plugin ids that this plugin's UI code imports modules from that are not in <code>requiredPlugins</code>. |
|  [requiredPlugins](./opensearch-dashboards.discoveredplugin.requiredplugins.md) | readonly [PluginName](./opensearch-dashboards.pluginname.md)<!-- -->\[\] | An optional list of the other plugins that \*\*must be\*\* installed and enabled for this plugin to function properly. |

