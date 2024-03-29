<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [RouteValidationResultFactory](./opensearch-dashboards.routevalidationresultfactory.md)

## RouteValidationResultFactory interface

Validation result factory to be used in the custom validation function to return the valid data or validation errors

See [RouteValidationFunction](./opensearch-dashboards.routevalidationfunction.md)<!-- -->.

<b>Signature:</b>

```typescript
export interface RouteValidationResultFactory 
```

## Properties

|  Property | Type | Description |
|  --- | --- | --- |
|  [badRequest](./opensearch-dashboards.routevalidationresultfactory.badrequest.md) | (error: Error \| string, path?: string\[\]) =&gt; { error: [RouteValidationError](./opensearch-dashboards.routevalidationerror.md)<!-- -->; } |  |
|  [ok](./opensearch-dashboards.routevalidationresultfactory.ok.md) | &lt;T&gt;(value: T) =&gt; { value: T; } |  |

