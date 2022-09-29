<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsFindOptions](./opensearch-dashboards.savedobjectsfindoptions.md) &gt; [rootSearchFields](./opensearch-dashboards.savedobjectsfindoptions.rootsearchfields.md)

## SavedObjectsFindOptions.rootSearchFields property

The fields to perform the parsed query against. Unlike the `searchFields` argument, these are expected to be root fields and will not be modified. If used in conjunction with `searchFields`<!-- -->, both are concatenated together.

<b>Signature:</b>

```typescript
rootSearchFields?: string[];
```