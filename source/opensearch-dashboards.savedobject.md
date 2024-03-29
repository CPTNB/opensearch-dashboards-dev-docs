<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObject](./opensearch-dashboards.savedobject.md)

## SavedObject interface

<b>Signature:</b>

```typescript
export interface SavedObject<T = unknown> 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [attributes](./opensearch-dashboards.savedobject.attributes.md) | T | The data for a Saved Object is stored as an object in the <code>attributes</code> property. |
|  [error?](./opensearch-dashboards.savedobject.error.md) | SavedObjectError | <i>(Optional)</i> |
|  [id](./opensearch-dashboards.savedobject.id.md) | string | The ID of this Saved Object, guaranteed to be unique for all objects of the same <code>type</code> |
|  [migrationVersion?](./opensearch-dashboards.savedobject.migrationversion.md) | [SavedObjectsMigrationVersion](./opensearch-dashboards.savedobjectsmigrationversion.md) | <i>(Optional)</i> Information about the migrations that have been applied to this SavedObject. When OpenSearch Dashboards starts up, OpenSearchDashboardsMigrator detects outdated documents and migrates them based on this value. For each migration that has been applied, the plugin's name is used as a key and the latest migration version as the value. |
|  [namespaces?](./opensearch-dashboards.savedobject.namespaces.md) | string\[\] | <i>(Optional)</i> Namespace(s) that this saved object exists in. This attribute is only used for multi-namespace saved object types. |
|  [originId?](./opensearch-dashboards.savedobject.originid.md) | string | <i>(Optional)</i> The ID of the saved object this originated from. This is set if this object's <code>id</code> was regenerated; that can happen during migration from a legacy single-namespace type, or during import. It is only set during migration or create operations. This is used during import to ensure that ID regeneration is deterministic, so saved objects will be overwritten if they are imported multiple times into a given space. |
|  [references](./opensearch-dashboards.savedobject.references.md) | [SavedObjectReference](./opensearch-dashboards.savedobjectreference.md)<!-- -->\[\] | A reference to another saved object. |
|  [type](./opensearch-dashboards.savedobject.type.md) | string | The type of Saved Object. Each plugin can define it's own custom Saved Object types. |
|  [updated\_at?](./opensearch-dashboards.savedobject.updated_at.md) | string | <i>(Optional)</i> Timestamp of the last time this document had been updated. |
|  [version?](./opensearch-dashboards.savedobject.version.md) | string | <i>(Optional)</i> An opaque version number which changes on each successful write operation. Can be used for implementing optimistic concurrency control. |

