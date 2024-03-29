<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsUpdateOptions](./opensearch-dashboards.savedobjectsupdateoptions.md)

## SavedObjectsUpdateOptions interface


<b>Signature:</b>

```typescript
export interface SavedObjectsUpdateOptions extends SavedObjectsBaseOptions 
```
<b>Extends:</b> [SavedObjectsBaseOptions](./opensearch-dashboards.savedobjectsbaseoptions.md)

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [references?](./opensearch-dashboards.savedobjectsupdateoptions.references.md) | [SavedObjectReference](./opensearch-dashboards.savedobjectreference.md)<!-- -->\[\] | <i>(Optional)</i> A reference to another saved object. |
|  [refresh?](./opensearch-dashboards.savedobjectsupdateoptions.refresh.md) | [MutatingOperationRefreshSetting](./opensearch-dashboards.mutatingoperationrefreshsetting.md) | <i>(Optional)</i> The OpenSearch Refresh setting for this operation |
|  [version?](./opensearch-dashboards.savedobjectsupdateoptions.version.md) | string | <i>(Optional)</i> An opaque version number which changes on each successful write operation. Can be used for implementing optimistic concurrency control. |

