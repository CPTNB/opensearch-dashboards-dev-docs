<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [OpenSearchDashboardsRequestRouteOptions](./opensearch-dashboards.opensearchdashboardsrequestrouteoptions.md)

## OpenSearchDashboardsRequestRouteOptions type

Route options: If 'GET' or 'OPTIONS' method, body options won't be returned.

<b>Signature:</b>

```typescript
export declare type OpenSearchDashboardsRequestRouteOptions<Method extends RouteMethod> = Method extends 'get' | 'options' ? Required<Omit<RouteConfigOptions<Method>, 'body'>> : Required<RouteConfigOptions<Method>>;
```
<b>References:</b> [RouteMethod](./opensearch-dashboards.routemethod.md)<!-- -->, [RouteConfigOptions](./opensearch-dashboards.routeconfigoptions.md)

