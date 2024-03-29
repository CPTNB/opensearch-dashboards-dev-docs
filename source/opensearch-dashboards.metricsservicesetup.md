<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [MetricsServiceSetup](./opensearch-dashboards.metricsservicesetup.md)

## MetricsServiceSetup interface

APIs to retrieves metrics gathered and exposed by the core platform.

<b>Signature:</b>

```typescript
export interface MetricsServiceSetup 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [collectionInterval](./opensearch-dashboards.metricsservicesetup.collectioninterval.md) | number | Interval metrics are collected in milliseconds |
|  [getOpsMetrics$](./opensearch-dashboards.metricsservicesetup.getopsmetrics_.md) | () =&gt; Observable&lt;[OpsMetrics](./opensearch-dashboards.opsmetrics.md)<!-- -->&gt; | Retrieve an observable emitting the [OpsMetrics](./opensearch-dashboards.opsmetrics.md) gathered. The observable will emit an initial value during core's <code>start</code> phase, and a new value every fixed interval of time, based on the <code>opts.interval</code> configuration property. |

