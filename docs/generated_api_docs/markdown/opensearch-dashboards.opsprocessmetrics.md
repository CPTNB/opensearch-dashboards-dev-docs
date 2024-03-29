<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [OpsProcessMetrics](./opensearch-dashboards.opsprocessmetrics.md)

## OpsProcessMetrics interface

Process related metrics

<b>Signature:</b>

```typescript
export interface OpsProcessMetrics 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [event\_loop\_delay](./opensearch-dashboards.opsprocessmetrics.event_loop_delay.md) | number | node event loop delay |
|  [memory](./opensearch-dashboards.opsprocessmetrics.memory.md) | { heap: { total\_in\_bytes: number; used\_in\_bytes: number; size\_limit: number; }; resident\_set\_size\_in\_bytes: number; } | process memory usage |
|  [pid](./opensearch-dashboards.opsprocessmetrics.pid.md) | number | pid of the OpenSearch Dashboards process |
|  [uptime\_in\_millis](./opensearch-dashboards.opsprocessmetrics.uptime_in_millis.md) | number | uptime of the OpenSearch Dashboards process |

