<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [CapabilitiesSetup](./opensearch-dashboards.capabilitiessetup.md)

## CapabilitiesSetup interface

APIs to manage the [Capabilities](./opensearch-dashboards.capabilities.md) that will be used by the application.

Plugins relying on capabilities to toggle some of their features should register them during the setup phase using the `registerProvider` method.

Plugins having the responsibility to restrict capabilities depending on a given context should register their capabilities switcher using the `registerSwitcher` method.

Refers to the methods documentation for complete description and examples.

<b>Signature:</b>

```typescript
export interface CapabilitiesSetup 
```

## Methods

|  Method | Description |
|  --- | --- |
|  [registerProvider(provider)](./opensearch-dashboards.capabilitiessetup.registerprovider.md) | Register a [CapabilitiesProvider](./opensearch-dashboards.capabilitiesprovider.md) to be used to provide [Capabilities](./opensearch-dashboards.capabilities.md) when resolving them. |
|  [registerSwitcher(switcher)](./opensearch-dashboards.capabilitiessetup.registerswitcher.md) | Register a [CapabilitiesSwitcher](./opensearch-dashboards.capabilitiesswitcher.md) to be used to change the default state of the [Capabilities](./opensearch-dashboards.capabilities.md) entries when resolving them.<!-- -->A capabilities switcher can only change the state of existing capabilities. Capabilities added or removed when invoking the switcher will be ignored. |
