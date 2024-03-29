<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [CoreSetup](./opensearch-dashboards.coresetup.md)

## CoreSetup interface

Context passed to the plugins `setup` method.

<b>Signature:</b>

```typescript
export interface CoreSetup<TPluginsStart extends object = object, TStart = unknown> 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [auditTrail](./opensearch-dashboards.coresetup.audittrail.md) | [AuditTrailSetup](./opensearch-dashboards.audittrailsetup.md) | [AuditTrailSetup](./opensearch-dashboards.audittrailsetup.md) |
|  [capabilities](./opensearch-dashboards.coresetup.capabilities.md) | [CapabilitiesSetup](./opensearch-dashboards.capabilitiessetup.md) | [CapabilitiesSetup](./opensearch-dashboards.capabilitiessetup.md) |
|  [context](./opensearch-dashboards.coresetup.context.md) | [ContextSetup](./opensearch-dashboards.contextsetup.md) | [ContextSetup](./opensearch-dashboards.contextsetup.md) |
|  [getStartServices](./opensearch-dashboards.coresetup.getstartservices.md) | [StartServicesAccessor](./opensearch-dashboards.startservicesaccessor.md)<!-- -->&lt;TPluginsStart, TStart&gt; | [StartServicesAccessor](./opensearch-dashboards.startservicesaccessor.md) |
|  [http](./opensearch-dashboards.coresetup.http.md) | [HttpServiceSetup](./opensearch-dashboards.httpservicesetup.md) &amp; { resources: [HttpResources](./opensearch-dashboards.httpresources.md)<!-- -->; } | [HttpServiceSetup](./opensearch-dashboards.httpservicesetup.md) |
|  [logging](./opensearch-dashboards.coresetup.logging.md) | [LoggingServiceSetup](./opensearch-dashboards.loggingservicesetup.md) | [LoggingServiceSetup](./opensearch-dashboards.loggingservicesetup.md) |
|  [metrics](./opensearch-dashboards.coresetup.metrics.md) | [MetricsServiceSetup](./opensearch-dashboards.metricsservicesetup.md) | [MetricsServiceSetup](./opensearch-dashboards.metricsservicesetup.md) |
|  [opensearch](./opensearch-dashboards.coresetup.opensearch.md) | [OpenSearchServiceSetup](./opensearch-dashboards.opensearchservicesetup.md) | [OpenSearchServiceSetup](./opensearch-dashboards.opensearchservicesetup.md) |
|  [savedObjects](./opensearch-dashboards.coresetup.savedobjects.md) | [SavedObjectsServiceSetup](./opensearch-dashboards.savedobjectsservicesetup.md) | [SavedObjectsServiceSetup](./opensearch-dashboards.savedobjectsservicesetup.md) |
|  [status](./opensearch-dashboards.coresetup.status.md) | [StatusServiceSetup](./opensearch-dashboards.statusservicesetup.md) | [StatusServiceSetup](./opensearch-dashboards.statusservicesetup.md) |
|  [uiSettings](./opensearch-dashboards.coresetup.uisettings.md) | [UiSettingsServiceSetup](./opensearch-dashboards.uisettingsservicesetup.md) | [UiSettingsServiceSetup](./opensearch-dashboards.uisettingsservicesetup.md) |

