<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [HttpServiceSetup](./opensearch-dashboards.httpservicesetup.md) &gt; [registerOnPreResponse](./opensearch-dashboards.httpservicesetup.registeronpreresponse.md)

## HttpServiceSetup.registerOnPreResponse property

To define custom logic to perform for the server response.

<b>Signature:</b>

```typescript
registerOnPreResponse: (handler: OnPreResponseHandler) => void;
```

## Remarks

Doesn't provide the whole response object. Supports extending response with custom headers. See [OnPreResponseHandler](./opensearch-dashboards.onpreresponsehandler.md)<!-- -->.

