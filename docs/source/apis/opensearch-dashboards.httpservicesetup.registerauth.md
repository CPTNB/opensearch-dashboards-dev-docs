<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [HttpServiceSetup](./opensearch-dashboards.httpservicesetup.md) &gt; [registerAuth](./opensearch-dashboards.httpservicesetup.registerauth.md)

## HttpServiceSetup.registerAuth property

To define custom authentication and/or authorization mechanism for incoming requests.

<b>Signature:</b>

```typescript
registerAuth: (handler: AuthenticationHandler) => void;
```

## Remarks

A handler should return a state to associate with the incoming request. The state can be retrieved later via http.auth.get(..) Only one AuthenticationHandler can be registered. See [AuthenticationHandler](./opensearch-dashboards.authenticationhandler.md)<!-- -->.

