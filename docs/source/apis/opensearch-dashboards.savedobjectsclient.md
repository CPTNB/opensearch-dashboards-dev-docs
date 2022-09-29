<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsClient](./opensearch-dashboards.savedobjectsclient.md)

## SavedObjectsClient class

<b>Signature:</b>

```typescript
export declare class SavedObjectsClient 
```

## Remarks

The constructor for this class is marked as internal. Third-party code should not call the constructor directly or create subclasses that extend the `SavedObjectsClient` class.

## Properties

|  Property | Modifiers | Type | Description |
|  --- | --- | --- | --- |
|  [errors](./opensearch-dashboards.savedobjectsclient.errors.md) |  | typeof [SavedObjectsErrorHelpers](./opensearch-dashboards.savedobjectserrorhelpers.md) |  |
|  [errors](./opensearch-dashboards.savedobjectsclient.errors.md) | <code>static</code> | typeof [SavedObjectsErrorHelpers](./opensearch-dashboards.savedobjectserrorhelpers.md) |  |

## Methods

|  Method | Modifiers | Description |
|  --- | --- | --- |
|  [addToNamespaces(type, id, namespaces, options)](./opensearch-dashboards.savedobjectsclient.addtonamespaces.md) |  | Adds namespaces to a SavedObject |
|  [bulkCreate(objects, options)](./opensearch-dashboards.savedobjectsclient.bulkcreate.md) |  | Persists multiple documents batched together as a single request |
|  [bulkGet(objects, options)](./opensearch-dashboards.savedobjectsclient.bulkget.md) |  | Returns an array of objects by id |
|  [bulkUpdate(objects, options)](./opensearch-dashboards.savedobjectsclient.bulkupdate.md) |  | Bulk Updates multiple SavedObject at once |
|  [checkConflicts(objects, options)](./opensearch-dashboards.savedobjectsclient.checkconflicts.md) |  | Check what conflicts will result when creating a given array of saved objects. This includes "unresolvable conflicts", which are multi-namespace objects that exist in a different namespace; such conflicts cannot be resolved/overwritten. |
|  [create(type, attributes, options)](./opensearch-dashboards.savedobjectsclient.create.md) |  | Persists a SavedObject |
|  [delete(type, id, options)](./opensearch-dashboards.savedobjectsclient.delete.md) |  | Deletes a SavedObject |
|  [deleteFromNamespaces(type, id, namespaces, options)](./opensearch-dashboards.savedobjectsclient.deletefromnamespaces.md) |  | Removes namespaces from a SavedObject |
|  [find(options)](./opensearch-dashboards.savedobjectsclient.find.md) |  | Find all SavedObjects matching the search query |
|  [get(type, id, options)](./opensearch-dashboards.savedobjectsclient.get.md) |  | Retrieves a single object |
|  [update(type, id, attributes, options)](./opensearch-dashboards.savedobjectsclient.update.md) |  | Updates an SavedObject |
