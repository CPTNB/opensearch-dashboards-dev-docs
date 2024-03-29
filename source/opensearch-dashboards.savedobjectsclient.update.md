<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsClient](./opensearch-dashboards.savedobjectsclient.md) &gt; [update](./opensearch-dashboards.savedobjectsclient.update.md)

## SavedObjectsClient.update() method

Updates an SavedObject

<b>Signature:</b>

```typescript
update<T = unknown>(type: string, id: string, attributes: Partial<T>, options?: SavedObjectsUpdateOptions): Promise<SavedObjectsUpdateResponse<T>>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  type | string |  |
|  id | string |  |
|  attributes | Partial&lt;T&gt; |  |
|  options | [SavedObjectsUpdateOptions](./opensearch-dashboards.savedobjectsupdateoptions.md) |  |

<b>Returns:</b>

Promise&lt;[SavedObjectsUpdateResponse](./opensearch-dashboards.savedobjectsupdateresponse.md)<!-- -->&lt;T&gt;&gt;

