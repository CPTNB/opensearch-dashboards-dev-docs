<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsTypeMappingDefinition](./opensearch-dashboards.savedobjectstypemappingdefinition.md)

## SavedObjectsTypeMappingDefinition interface

Describe a saved object type mapping.

<b>Signature:</b>

```typescript
export interface SavedObjectsTypeMappingDefinition 
```

## Example


```ts
const typeDefinition: SavedObjectsTypeMappingDefinition = {
  properties: {
    enabled: {
      type: "boolean"
    },
    sendUsageFrom: {
      ignore_above: 256,
      type: "keyword"
    },
    lastReported: {
      type: "date"
    },
    lastVersionChecked: {
      ignore_above: 256,
      type: "keyword"
    },
  }
}
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [dynamic?](./opensearch-dashboards.savedobjectstypemappingdefinition.dynamic.md) | false \| 'strict' | <i>(Optional)</i> The dynamic property of the mapping, either <code>false</code> or <code>'strict'</code>. If unspecified <code>dynamic: 'strict'</code> will be inherited from the top-level index mappings. |
|  [properties](./opensearch-dashboards.savedobjectstypemappingdefinition.properties.md) | [SavedObjectsMappingProperties](./opensearch-dashboards.savedobjectsmappingproperties.md) | The underlying properties of the type mapping |

