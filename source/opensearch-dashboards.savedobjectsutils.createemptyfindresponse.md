<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsUtils](./opensearch-dashboards.savedobjectsutils.md) &gt; [createEmptyFindResponse](./opensearch-dashboards.savedobjectsutils.createemptyfindresponse.md)

## SavedObjectsUtils.createEmptyFindResponse property

Creates an empty response for a find operation. This is only intended to be used by saved objects client wrappers.

<b>Signature:</b>

```typescript
static createEmptyFindResponse: <T>({ page, perPage, }: SavedObjectsFindOptions) => SavedObjectsFindResponse<T>;
```