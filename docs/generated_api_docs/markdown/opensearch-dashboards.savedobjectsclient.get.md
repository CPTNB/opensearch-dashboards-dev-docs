<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsClient](./opensearch-dashboards.savedobjectsclient.md) &gt; [get](./opensearch-dashboards.savedobjectsclient.get.md)

## SavedObjectsClient.get() method

Retrieves a single object

<b>Signature:</b>

```typescript
get<T = unknown>(type: string, id: string, options?: SavedObjectsBaseOptions): Promise<SavedObject<T>>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  type | string | The type of SavedObject to retrieve |
|  id | string | The ID of the SavedObject to retrieve |
|  options | [SavedObjectsBaseOptions](./opensearch-dashboards.savedobjectsbaseoptions.md) |  |

<b>Returns:</b>

Promise&lt;[SavedObject](./opensearch-dashboards.savedobject.md)<!-- -->&lt;T&gt;&gt;

