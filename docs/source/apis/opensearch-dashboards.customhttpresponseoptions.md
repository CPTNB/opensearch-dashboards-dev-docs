<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [CustomHttpResponseOptions](./opensearch-dashboards.customhttpresponseoptions.md)

## CustomHttpResponseOptions interface

HTTP response parameters for a response with adjustable status code.

<b>Signature:</b>

```typescript
export interface CustomHttpResponseOptions<T extends HttpResponsePayload | ResponseError> 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [body?](./opensearch-dashboards.customhttpresponseoptions.body.md) | T | <i>(Optional)</i> HTTP message to send to the client |
|  [headers?](./opensearch-dashboards.customhttpresponseoptions.headers.md) | [ResponseHeaders](./opensearch-dashboards.responseheaders.md) | <i>(Optional)</i> HTTP Headers with additional information about response |
|  [statusCode](./opensearch-dashboards.customhttpresponseoptions.statuscode.md) | number |  |

