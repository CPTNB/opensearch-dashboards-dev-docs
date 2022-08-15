<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsClient](./opensearch-dashboards.savedobjectsclient.md) &gt; [deleteFromNamespaces](./opensearch-dashboards.savedobjectsclient.deletefromnamespaces.md)

## SavedObjectsClient.deleteFromNamespaces() method

Removes namespaces from a SavedObject

<b>Signature:</b>

```typescript
deleteFromNamespaces(type: string, id: string, namespaces: string[], options?: SavedObjectsDeleteFromNamespacesOptions): Promise<SavedObjectsDeleteFromNamespacesResponse>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  type | string |  |
|  id | string |  |
|  namespaces | string\[\] |  |
|  options | [SavedObjectsDeleteFromNamespacesOptions](./opensearch-dashboards.savedobjectsdeletefromnamespacesoptions.md) |  |

<b>Returns:</b>

Promise&lt;[SavedObjectsDeleteFromNamespacesResponse](./opensearch-dashboards.savedobjectsdeletefromnamespacesresponse.md)<!-- -->&gt;
