<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [Headers\_2](./opensearch-dashboards.headers_2.md)

## Headers\_2 type

Http request headers to read.

<b>Signature:</b>

```typescript
export declare type Headers = {
    [header in KnownHeaders]?: string | string[] | undefined;
} & {
    [header: string]: string | string[] | undefined;
};
```
<b>References:</b> [KnownHeaders](./opensearch-dashboards.knownheaders.md)
