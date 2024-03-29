<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsRepository](./opensearch-dashboards.savedobjectsrepository.md) &gt; [deleteByNamespace](./opensearch-dashboards.savedobjectsrepository.deletebynamespace.md)

## SavedObjectsRepository.deleteByNamespace() method

Deletes all objects from the provided namespace.

<b>Signature:</b>

```typescript
deleteByNamespace(namespace: string, options?: SavedObjectsDeleteByNamespaceOptions): Promise<any>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  namespace | string |  |
|  options | [SavedObjectsDeleteByNamespaceOptions](./opensearch-dashboards.savedobjectsdeletebynamespaceoptions.md) |  |

<b>Returns:</b>

Promise&lt;any&gt;

{<!-- -->promise<!-- -->} - { took, timed\_out, total, deleted, batches, version\_conflicts, noops, retries, failures }

