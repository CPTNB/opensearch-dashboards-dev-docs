<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsRepository](./opensearch-dashboards.savedobjectsrepository.md) &gt; [bulkGet](./opensearch-dashboards.savedobjectsrepository.bulkget.md)

## SavedObjectsRepository.bulkGet() method

Returns an array of objects by id

<b>Signature:</b>

```typescript
bulkGet<T = unknown>(objects?: SavedObjectsBulkGetObject[], options?: SavedObjectsBaseOptions): Promise<SavedObjectsBulkResponse<T>>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  objects | [SavedObjectsBulkGetObject](./opensearch-dashboards.savedobjectsbulkgetobject.md)<!-- -->\[\] | an array of objects containing id, type and optionally fields |
|  options | [SavedObjectsBaseOptions](./opensearch-dashboards.savedobjectsbaseoptions.md) |  {<!-- -->string<!-- -->} \[options.namespace\] |

<b>Returns:</b>

Promise&lt;[SavedObjectsBulkResponse](./opensearch-dashboards.savedobjectsbulkresponse.md)<!-- -->&lt;T&gt;&gt;

{<!-- -->promise<!-- -->} - { saved\_objects: \[{ id, type, version, attributes }<!-- -->\] }

## Example

bulkGet(\[ { id: 'one', type: 'config' }<!-- -->, { id: 'foo', type: 'index-pattern' } \])

