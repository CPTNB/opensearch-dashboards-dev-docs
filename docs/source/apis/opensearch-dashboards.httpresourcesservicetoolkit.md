<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [HttpResourcesServiceToolkit](./opensearch-dashboards.httpresourcesservicetoolkit.md)

## HttpResourcesServiceToolkit interface

Extended set of [OpenSearchDashboardsResponseFactory](./opensearch-dashboards.opensearchdashboardsresponsefactory.md) helpers used to respond with HTML or JS resource.

<b>Signature:</b>

```typescript
export interface HttpResourcesServiceToolkit 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [renderAnonymousCoreApp](./opensearch-dashboards.httpresourcesservicetoolkit.renderanonymouscoreapp.md) | (options?: [HttpResourcesRenderOptions](./opensearch-dashboards.httpresourcesrenderoptions.md)<!-- -->) =&gt; Promise&lt;[IOpenSearchDashboardsResponse](./opensearch-dashboards.iopensearchdashboardsresponse.md)<!-- -->&gt; | To respond with HTML page bootstrapping OpenSearch Dashboards application without retrieving user-specific information. |
|  [renderCoreApp](./opensearch-dashboards.httpresourcesservicetoolkit.rendercoreapp.md) | (options?: [HttpResourcesRenderOptions](./opensearch-dashboards.httpresourcesrenderoptions.md)<!-- -->) =&gt; Promise&lt;[IOpenSearchDashboardsResponse](./opensearch-dashboards.iopensearchdashboardsresponse.md)<!-- -->&gt; | To respond with HTML page bootstrapping OpenSearch Dashboards application. |
|  [renderHtml](./opensearch-dashboards.httpresourcesservicetoolkit.renderhtml.md) | (options: [HttpResourcesResponseOptions](./opensearch-dashboards.httpresourcesresponseoptions.md)<!-- -->) =&gt; [IOpenSearchDashboardsResponse](./opensearch-dashboards.iopensearchdashboardsresponse.md) | To respond with a custom HTML page. |
|  [renderJs](./opensearch-dashboards.httpresourcesservicetoolkit.renderjs.md) | (options: [HttpResourcesResponseOptions](./opensearch-dashboards.httpresourcesresponseoptions.md)<!-- -->) =&gt; [IOpenSearchDashboardsResponse](./opensearch-dashboards.iopensearchdashboardsresponse.md) | To respond with a custom JS script file. |

