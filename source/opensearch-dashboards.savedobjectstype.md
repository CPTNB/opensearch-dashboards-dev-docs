<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsType](./opensearch-dashboards.savedobjectstype.md)

## SavedObjectsType interface

<b>Signature:</b>

```typescript
export interface SavedObjectsType 
```

## Remarks

This is only internal for now, and will only be public when we expose the registerType API

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [convertToAliasScript?](./opensearch-dashboards.savedobjectstype.converttoaliasscript.md) | string | <i>(Optional)</i> If defined, will be used to convert the type to an alias. |
|  [hidden](./opensearch-dashboards.savedobjectstype.hidden.md) | boolean | Is the type hidden by default. If true, repositories will not have access to this type unless explicitly declared as an <code>extraType</code> when creating the repository.<!-- -->See [createInternalRepository](./opensearch-dashboards.savedobjectsservicestart.createinternalrepository.md)<!-- -->. |
|  [indexPattern?](./opensearch-dashboards.savedobjectstype.indexpattern.md) | string | <i>(Optional)</i> If defined, the type instances will be stored in the given index instead of the default one. |
|  [management?](./opensearch-dashboards.savedobjectstype.management.md) | [SavedObjectsTypeManagementDefinition](./opensearch-dashboards.savedobjectstypemanagementdefinition.md) | <i>(Optional)</i> An optional [saved objects management section](./opensearch-dashboards.savedobjectstypemanagementdefinition.md) definition for the type. |
|  [mappings](./opensearch-dashboards.savedobjectstype.mappings.md) | [SavedObjectsTypeMappingDefinition](./opensearch-dashboards.savedobjectstypemappingdefinition.md) | The [mapping definition](./opensearch-dashboards.savedobjectstypemappingdefinition.md) for the type. |
|  [migrations?](./opensearch-dashboards.savedobjectstype.migrations.md) | [SavedObjectMigrationMap](./opensearch-dashboards.savedobjectmigrationmap.md) | <i>(Optional)</i> An optional map of [migrations](./opensearch-dashboards.savedobjectmigrationfn.md) to be used to migrate the type. |
|  [name](./opensearch-dashboards.savedobjectstype.name.md) | string | The name of the type, which is also used as the internal id. |
|  [namespaceType](./opensearch-dashboards.savedobjectstype.namespacetype.md) | [SavedObjectsNamespaceType](./opensearch-dashboards.savedobjectsnamespacetype.md) | The [namespace type](./opensearch-dashboards.savedobjectsnamespacetype.md) for the type. |

