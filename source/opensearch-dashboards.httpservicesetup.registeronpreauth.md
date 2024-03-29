<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [HttpServiceSetup](./opensearch-dashboards.httpservicesetup.md) &gt; [registerOnPreAuth](./opensearch-dashboards.httpservicesetup.registeronpreauth.md)

## HttpServiceSetup.registerOnPreAuth property

To define custom logic to perform for incoming requests before the Auth interceptor performs a check that user has access to requested resources.

<b>Signature:</b>

```typescript
registerOnPreAuth: (handler: OnPreAuthHandler) => void;
```

## Remarks

Can register any number of registerOnPreAuth, which are called in sequence (from the first registered to the last). See [OnPreAuthHandler](./opensearch-dashboards.onpreauthhandler.md)<!-- -->.

