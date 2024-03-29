<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsRepository](./opensearch-dashboards.savedobjectsrepository.md) &gt; [bulkUpdate](./opensearch-dashboards.savedobjectsrepository.bulkupdate.md)

## SavedObjectsRepository.bulkUpdate() method

Updates multiple objects in bulk

<b>Signature:</b>

```typescript
bulkUpdate<T = unknown>(objects: Array<SavedObjectsBulkUpdateObject<T>>, options?: SavedObjectsBulkUpdateOptions): Promise<SavedObjectsBulkUpdateResponse<T>>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  objects | Array&lt;[SavedObjectsBulkUpdateObject](./opensearch-dashboards.savedobjectsbulkupdateobject.md)<!-- -->&lt;T&gt;&gt; | \[{ type, id, attributes, options: { version, namespace } references }<!-- -->\]  {<!-- -->string<!-- -->} options.version - ensures version matches that of persisted object  {<!-- -->string<!-- -->} \[options.namespace\] |
|  options | [SavedObjectsBulkUpdateOptions](./opensearch-dashboards.savedobjectsbulkupdateoptions.md) |  |

<b>Returns:</b>

Promise&lt;[SavedObjectsBulkUpdateResponse](./opensearch-dashboards.savedobjectsbulkupdateresponse.md)<!-- -->&lt;T&gt;&gt;

{<!-- -->promise<!-- -->} - {<!-- -->saved\_objects: \[\[{ id, type, version, references, attributes, error: { message } }<!-- -->\]<!-- -->}

