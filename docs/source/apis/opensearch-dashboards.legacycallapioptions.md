<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [LegacyCallAPIOptions](./opensearch-dashboards.legacycallapioptions.md)

## LegacyCallAPIOptions interface

> Warning: This API is now obsolete.
> 
> 

The set of options that defines how API call should be made and result be processed.

<b>Signature:</b>

```typescript
export interface LegacyCallAPIOptions 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [signal?](./opensearch-dashboards.legacycallapioptions.signal.md) | AbortSignal | <i>(Optional)</i> A signal object that allows you to abort the request via an AbortController object. |
|  [wrap401Errors?](./opensearch-dashboards.legacycallapioptions.wrap401errors.md) | boolean | <i>(Optional)</i> Indicates whether <code>401 Unauthorized</code> errors returned from the OpenSearch API should be wrapped into <code>Boom</code> error instances with properly set <code>WWW-Authenticate</code> header that could have been returned by the API itself. If API didn't specify that then <code>Basic realm=&quot;Authorization Required&quot;</code> is used as <code>WWW-Authenticate</code>. |

