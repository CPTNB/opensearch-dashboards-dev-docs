<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [RouteConfigOptions](./opensearch-dashboards.routeconfigoptions.md)

## RouteConfigOptions interface

Additional route options.

<b>Signature:</b>

```typescript
export interface RouteConfigOptions<Method extends RouteMethod> 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [authRequired?](./opensearch-dashboards.routeconfigoptions.authrequired.md) | boolean \| 'optional' | <i>(Optional)</i> Defines authentication mode for a route: - true. A user has to have valid credentials to access a resource - false. A user can access a resource without any credentials. - 'optional'. A user can access a resource if has valid credentials or no credentials at all. Can be useful when we grant access to a resource but want to identify a user if possible.<!-- -->Defaults to <code>true</code> if an auth mechanism is registered. |
|  [body?](./opensearch-dashboards.routeconfigoptions.body.md) | Method extends 'get' \| 'options' ? undefined : [RouteConfigOptionsBody](./opensearch-dashboards.routeconfigoptionsbody.md) | <i>(Optional)</i> Additional body options [RouteConfigOptionsBody](./opensearch-dashboards.routeconfigoptionsbody.md)<!-- -->. |
|  [tags?](./opensearch-dashboards.routeconfigoptions.tags.md) | readonly string\[\] | <i>(Optional)</i> Additional metadata tag strings to attach to the route. |
|  [timeout?](./opensearch-dashboards.routeconfigoptions.timeout.md) | { payload?: Method extends 'get' \| 'options' ? undefined : number; idleSocket?: number; } | <i>(Optional)</i> Defines per-route timeouts. |
|  [xsrfRequired?](./opensearch-dashboards.routeconfigoptions.xsrfrequired.md) | Method extends 'get' ? never : boolean | <i>(Optional)</i> Defines xsrf protection requirements for a route: - true. Requires an incoming POST/PUT/DELETE request to contain <code>osd-xsrf</code> header. - false. Disables xsrf protection.<!-- -->Set to true by default |

