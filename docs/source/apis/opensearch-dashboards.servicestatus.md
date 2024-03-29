<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [ServiceStatus](./opensearch-dashboards.servicestatus.md)

## ServiceStatus interface

The current status of a service at a point in time.

<b>Signature:</b>

```typescript
export interface ServiceStatus<Meta extends Record<string, any> | unknown = unknown> 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [detail?](./opensearch-dashboards.servicestatus.detail.md) | string | <i>(Optional)</i> A more detailed description of the service status. |
|  [documentationUrl?](./opensearch-dashboards.servicestatus.documentationurl.md) | string | <i>(Optional)</i> A URL to open in a new tab about how to resolve or troubleshoot the problem. |
|  [level](./opensearch-dashboards.servicestatus.level.md) | [ServiceStatusLevel](./opensearch-dashboards.servicestatuslevel.md) | The current availability level of the service. |
|  [meta?](./opensearch-dashboards.servicestatus.meta.md) | Meta | <i>(Optional)</i> Any JSON-serializable data to be included in the HTTP API response. Useful for providing more fine-grained, machine-readable information about the service status. May include status information for underlying features. |
|  [summary](./opensearch-dashboards.servicestatus.summary.md) | string | A high-level summary of the service status. |

