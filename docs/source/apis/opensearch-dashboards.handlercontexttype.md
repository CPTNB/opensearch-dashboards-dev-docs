<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [HandlerContextType](./opensearch-dashboards.handlercontexttype.md)

## HandlerContextType type

Extracts the type of the first argument of a [HandlerFunction](./opensearch-dashboards.handlerfunction.md) to represent the type of the context.

<b>Signature:</b>

```typescript
export declare type HandlerContextType<T extends HandlerFunction<any>> = T extends HandlerFunction<infer U> ? U : never;
```
<b>References:</b> [HandlerFunction](./opensearch-dashboards.handlerfunction.md)

