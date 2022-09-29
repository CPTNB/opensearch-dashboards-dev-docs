<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [RouteConfigOptionsBody](./opensearch-dashboards.routeconfigoptionsbody.md) &gt; [output](./opensearch-dashboards.routeconfigoptionsbody.output.md)

## RouteConfigOptionsBody.output property

The processed payload format. The value must be one of: \* 'data' - the incoming payload is read fully into memory. If parse is true, the payload is parsed (JSON, form-decoded, multipart) based on the 'Content-Type' header. If parse is false, a raw Buffer is returned. \* 'stream' - the incoming payload is made available via a Stream.Readable interface. If the payload is 'multipart/form-data' and parse is true, field values are presented as text while files are provided as streams. File streams from a 'multipart/form-data' upload will also have a hapi property containing the filename and headers properties. Note that payload streams for multipart payloads are a synthetic interface created on top of the entire multipart content loaded into memory. To avoid loading large multipart payloads into memory, set parse to false and handle the multipart payload in the handler using a streaming parser (e.g. pez).

Default value: 'data', unless no validation.body is provided in the route definition. In that case the default is 'stream' to alleviate memory pressure.

<b>Signature:</b>

```typescript
output?: typeof validBodyOutput[number];
```