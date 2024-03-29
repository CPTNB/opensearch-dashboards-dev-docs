<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [OpsOsMetrics](./opensearch-dashboards.opsosmetrics.md)

## OpsOsMetrics interface

OS related metrics

<b>Signature:</b>

```typescript
export interface OpsOsMetrics 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [cpu?](./opensearch-dashboards.opsosmetrics.cpu.md) | { control\_group: string; cfs\_period\_micros: number; cfs\_quota\_micros: number; stat: { number\_of\_elapsed\_periods: number; number\_of\_times\_throttled: number; time\_throttled\_nanos: number; }; } | <i>(Optional)</i> cpu cgroup metrics, undefined when not running in a cgroup |
|  [cpuacct?](./opensearch-dashboards.opsosmetrics.cpuacct.md) | { control\_group: string; usage\_nanos: number; } | <i>(Optional)</i> cpu accounting metrics, undefined when not running in a cgroup |
|  [distro?](./opensearch-dashboards.opsosmetrics.distro.md) | string | <i>(Optional)</i> The os distrib. Only present for linux platforms |
|  [distroRelease?](./opensearch-dashboards.opsosmetrics.distrorelease.md) | string | <i>(Optional)</i> The os distrib release, prefixed by the os distrib. Only present for linux platforms |
|  [load](./opensearch-dashboards.opsosmetrics.load.md) | { '1m': number; '5m': number; '15m': number; } | cpu load metrics |
|  [memory](./opensearch-dashboards.opsosmetrics.memory.md) | { total\_in\_bytes: number; free\_in\_bytes: number; used\_in\_bytes: number; } | system memory usage metrics |
|  [platform](./opensearch-dashboards.opsosmetrics.platform.md) | NodeJS.Platform | The os platform |
|  [platformRelease](./opensearch-dashboards.opsosmetrics.platformrelease.md) | string | The os platform release, prefixed by the platform name |
|  [uptime\_in\_millis](./opensearch-dashboards.opsosmetrics.uptime_in_millis.md) | number | the OS uptime |

