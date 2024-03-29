<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [CapabilitiesSetup](./opensearch-dashboards.capabilitiessetup.md) &gt; [registerProvider](./opensearch-dashboards.capabilitiessetup.registerprovider.md)

## CapabilitiesSetup.registerProvider() method

Register a [CapabilitiesProvider](./opensearch-dashboards.capabilitiesprovider.md) to be used to provide [Capabilities](./opensearch-dashboards.capabilities.md) when resolving them.

<b>Signature:</b>

```typescript
registerProvider(provider: CapabilitiesProvider): void;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  provider | [CapabilitiesProvider](./opensearch-dashboards.capabilitiesprovider.md) |  |

<b>Returns:</b>

void

## Example

How to register a plugin's capabilities during setup

```ts
// my-plugin/server/plugin.ts
public setup(core: CoreSetup, deps: {}) {
   core.capabilities.registerProvider(() => {
     return {
       catalogue: {
         myPlugin: true,
       },
       myPlugin: {
         someFeature: true,
         featureDisabledByDefault: false,
       },
     }
   });
}
```

