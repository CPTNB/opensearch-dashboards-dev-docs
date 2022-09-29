<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsRepository](./opensearch-dashboards.savedobjectsrepository.md) &gt; [update](./opensearch-dashboards.savedobjectsrepository.update.md)

## SavedObjectsRepository.update() method

Updates an object

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
|  options | [SavedObjectsUpdateOptions](./opensearch-dashboards.savedobjectsupdateoptions.md) |  {<!-- -->string<!-- -->} options.version - ensures version matches that of persisted object  {<!-- -->string<!-- -->} \[options.namespace\]  {<!-- -->array<!-- -->} \[options.references\] - \[{ name, type, id }<!-- -->\] |

<b>Returns:</b>

Promise&lt;[SavedObjectsUpdateResponse](./opensearch-dashboards.savedobjectsupdateresponse.md)<!-- -->&lt;T&gt;&gt;

{<!-- -->promise<!-- -->}
