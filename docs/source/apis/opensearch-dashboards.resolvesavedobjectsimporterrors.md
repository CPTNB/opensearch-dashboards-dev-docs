<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [resolveSavedObjectsImportErrors](./opensearch-dashboards.resolvesavedobjectsimporterrors.md)

## resolveSavedObjectsImportErrors() function

Resolve and return saved object import errors. See the [options](./opensearch-dashboards.savedobjectsresolveimporterrorsoptions.md) for more detailed informations.

<b>Signature:</b>

```typescript
export declare function resolveSavedObjectsImportErrors({ readStream, objectLimit, retries, savedObjectsClient, typeRegistry, namespace, createNewCopies, }: SavedObjectsResolveImportErrorsOptions): Promise<SavedObjectsImportResponse>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  { readStream, objectLimit, retries, savedObjectsClient, typeRegistry, namespace, createNewCopies, } | [SavedObjectsResolveImportErrorsOptions](./opensearch-dashboards.savedobjectsresolveimporterrorsoptions.md) |  |

<b>Returns:</b>

Promise&lt;[SavedObjectsImportResponse](./opensearch-dashboards.savedobjectsimportresponse.md)<!-- -->&gt;

