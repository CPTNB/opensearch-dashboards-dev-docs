<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [HttpResources](./opensearch-dashboards.httpresources.md)

## HttpResources interface

HttpResources service is responsible for serving static &amp; dynamic assets for OpenSearch Dashboards application via HTTP. Provides API allowing plug-ins to respond with: - a pre-configured HTML page bootstrapping OpenSearch Dashboards client app - custom HTML page - custom JS script file.

<b>Signature:</b>

```typescript
export interface HttpResources 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [register](./opensearch-dashboards.httpresources.register.md) | &lt;P, Q, B&gt;(route: [RouteConfig](./opensearch-dashboards.routeconfig.md)<!-- -->&lt;P, Q, B, 'get'&gt;, handler: [HttpResourcesRequestHandler](./opensearch-dashboards.httpresourcesrequesthandler.md)<!-- -->&lt;P, Q, B&gt;) =&gt; void | To register a route handler executing passed function to form response. |

