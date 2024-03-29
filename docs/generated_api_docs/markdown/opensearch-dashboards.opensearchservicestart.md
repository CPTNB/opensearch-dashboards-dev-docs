<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [OpenSearchServiceStart](./opensearch-dashboards.opensearchservicestart.md)

## OpenSearchServiceStart interface


<b>Signature:</b>

```typescript
export interface OpenSearchServiceStart 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [client](./opensearch-dashboards.opensearchservicestart.client.md) | [IClusterClient](./opensearch-dashboards.iclusterclient.md) | A pre-configured [OpenSearch client](./opensearch-dashboards.iclusterclient.md) |
|  [createClient](./opensearch-dashboards.opensearchservicestart.createclient.md) | (type: string, clientConfig?: Partial&lt;[OpenSearchClientConfig](./opensearch-dashboards.opensearchclientconfig.md)<!-- -->&gt;) =&gt; [ICustomClusterClient](./opensearch-dashboards.icustomclusterclient.md) | Create application specific OpenSearch cluster API client with customized config. See [IClusterClient](./opensearch-dashboards.iclusterclient.md)<!-- -->. |
|  [legacy](./opensearch-dashboards.opensearchservicestart.legacy.md) | { readonly config$: Observable&lt;[OpenSearchConfig](./opensearch-dashboards.opensearchconfig.md)<!-- -->&gt;; readonly createClient: (type: string, clientConfig?: Partial&lt;[LegacyOpenSearchClientConfig](./opensearch-dashboards.legacyopensearchclientconfig.md)<!-- -->&gt;) =&gt; [ILegacyCustomClusterClient](./opensearch-dashboards.ilegacycustomclusterclient.md)<!-- -->; readonly client: [ILegacyClusterClient](./opensearch-dashboards.ilegacyclusterclient.md)<!-- -->; } |  |

