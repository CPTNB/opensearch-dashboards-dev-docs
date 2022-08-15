<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [PluginManifest](./opensearch-dashboards.pluginmanifest.md)

## PluginManifest interface

Describes the set of required and optional properties plugin can define in its mandatory JSON manifest file.

<b>Signature:</b>

```typescript
export interface PluginManifest 
```

## Remarks

Should never be used in code outside of Core but is exported for documentation purposes.

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [configPath](./opensearch-dashboards.pluginmanifest.configpath.md) | ConfigPath | Root  used by the plugin, defaults to "id" in snake\_case format. |
|  [extraPublicDirs?](./opensearch-dashboards.pluginmanifest.extrapublicdirs.md) | string\[\] | <i>(Optional)</i> Specifies directory names that can be imported by other ui-plugins built using the same instance of the @<!-- -->osd/optimizer. A temporary measure we plan to replace with better mechanisms for sharing static code between plugins |
|  [id](./opensearch-dashboards.pluginmanifest.id.md) | [PluginName](./opensearch-dashboards.pluginname.md) | Identifier of the plugin. Must be a string in camelCase. Part of a plugin public contract. Other plugins leverage it to access plugin API, navigate to the plugin, etc. |
|  [opensearchDashboardsVersion](./opensearch-dashboards.pluginmanifest.opensearchdashboardsversion.md) | string | The version of OpenSearch Dashboards the plugin is compatible with, defaults to "version". |
|  [optionalPlugins](./opensearch-dashboards.pluginmanifest.optionalplugins.md) | readonly [PluginName](./opensearch-dashboards.pluginname.md)<!-- -->\[\] | An optional list of the other plugins that if installed and enabled \*\*may be\*\* leveraged by this plugin for some additional functionality but otherwise are not required for this plugin to work properly. |
|  [requiredBundles](./opensearch-dashboards.pluginmanifest.requiredbundles.md) | readonly string\[\] | List of plugin ids that this plugin's UI code imports modules from that are not in <code>requiredPlugins</code>. |
|  [requiredPlugins](./opensearch-dashboards.pluginmanifest.requiredplugins.md) | readonly [PluginName](./opensearch-dashboards.pluginname.md)<!-- -->\[\] | An optional list of the other plugins that \*\*must be\*\* installed and enabled for this plugin to function properly. |
|  [server](./opensearch-dashboards.pluginmanifest.server.md) | boolean | Specifies whether plugin includes some server-side specific functionality. |
|  [ui](./opensearch-dashboards.pluginmanifest.ui.md) | boolean | Specifies whether plugin includes some client/browser specific functionality that should be included into client bundle via <code>public/ui_plugin.js</code> file. |
|  [version](./opensearch-dashboards.pluginmanifest.version.md) | string | Version of the plugin. |
