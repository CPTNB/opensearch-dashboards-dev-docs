<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsNamespaceType](./opensearch-dashboards.savedobjectsnamespacetype.md)

## SavedObjectsNamespaceType type

The namespace type dictates how a saved object can be interacted in relation to namespaces. Each type is mutually exclusive: \* single (default): this type of saved object is namespace-isolated, e.g., it exists in only one namespace. \* multiple: this type of saved object is shareable, e.g., it can exist in one or more namespaces. \* agnostic: this type of saved object is global.

<b>Signature:</b>

```typescript
export declare type SavedObjectsNamespaceType = 'single' | 'multiple' | 'agnostic';
```
