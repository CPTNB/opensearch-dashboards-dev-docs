<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [SavedObjectsRepository](./opensearch-dashboards.savedobjectsrepository.md) &gt; [incrementCounter](./opensearch-dashboards.savedobjectsrepository.incrementcounter.md)

## SavedObjectsRepository.incrementCounter() method

Increases a counter field by one. Creates the document if one doesn't exist for the given id.

<b>Signature:</b>

```typescript
incrementCounter(type: string, id: string, counterFieldName: string, options?: SavedObjectsIncrementCounterOptions): Promise<SavedObject>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  type | string |  |
|  id | string |  |
|  counterFieldName | string |  |
|  options | [SavedObjectsIncrementCounterOptions](./opensearch-dashboards.savedobjectsincrementcounteroptions.md) |  {<!-- -->object<!-- -->} \[options.migrationVersion=undefined\] |

<b>Returns:</b>

Promise&lt;[SavedObject](./opensearch-dashboards.savedobject.md)<!-- -->&gt;

{<!-- -->promise<!-- -->}
