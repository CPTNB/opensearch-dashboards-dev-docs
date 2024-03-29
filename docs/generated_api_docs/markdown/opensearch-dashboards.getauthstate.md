<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [GetAuthState](./opensearch-dashboards.getauthstate.md)

## GetAuthState type

Gets authentication state for a request. Returned by `auth` interceptor.

<b>Signature:</b>

```typescript
export declare type GetAuthState = <T = unknown>(request: OpenSearchDashboardsRequest | LegacyRequest) => {
    status: AuthStatus;
    state: T;
};
```
<b>References:</b> [OpenSearchDashboardsRequest](./opensearch-dashboards.opensearchdashboardsrequest.md)<!-- -->, [LegacyRequest](./opensearch-dashboards.legacyrequest.md)<!-- -->, [AuthStatus](./opensearch-dashboards.authstatus.md)

