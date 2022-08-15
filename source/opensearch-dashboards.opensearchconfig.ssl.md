<!-- Do not edit this file. It is automatically generated by API Documenter. -->

[Home](./index.md) &gt; [opensearch-dashboards](./opensearch-dashboards.md) &gt; [OpenSearchConfig](./opensearch-dashboards.opensearchconfig.md) &gt; [ssl](./opensearch-dashboards.opensearchconfig.ssl.md)

## OpenSearchConfig.ssl property

Set of settings configure SSL connection between OpenSearch Dashboards and OpenSearch that are required when `xpack.ssl.verification_mode` in OpenSearch is set to either `certificate` or `full`<!-- -->.

<b>Signature:</b>

```typescript
readonly ssl: Pick<SslConfigSchema, Exclude<keyof SslConfigSchema, 'certificateAuthorities' | 'keystore' | 'truststore'>> & {
        certificateAuthorities?: string[];
    };
```