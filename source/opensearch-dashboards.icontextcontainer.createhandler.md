<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [IContextContainer](./opensearch-dashboards.icontextcontainer.md) &gt; [createHandler](./opensearch-dashboards.icontextcontainer.createhandler.md)

## IContextContainer.createHandler() method

Create a new handler function pre-wired to context for the plugin.

<b>Signature:</b>

```typescript
createHandler(pluginOpaqueId: PluginOpaqueId, handler: THandler): (...rest: HandlerParameters<THandler>) => ShallowPromise<ReturnType<THandler>>;
```

## Parameters

|  Parameter | Type | Description |
|  --- | --- | --- |
|  pluginOpaqueId | [PluginOpaqueId](./opensearch-dashboards.pluginopaqueid.md) | The plugin opaque ID for the plugin that registers this handler. |
|  handler | THandler | Handler function to pass context object to. |

<b>Returns:</b>

(...rest: [HandlerParameters](./opensearch-dashboards.handlerparameters.md)<!-- -->&lt;THandler&gt;) =&gt; ShallowPromise&lt;ReturnType&lt;THandler&gt;&gt;

A function that takes `THandlerParameters`<!-- -->, calls `handler` with a new context, and returns a Promise of the `handler` return value.
