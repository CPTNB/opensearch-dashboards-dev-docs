# Building OpenSearch Dashboards

## Release version
This section is for building a release version of OpenSearch Dashboards. The release version is the compiled down JavaScript files.

### Linux x64
To build a release version for Linux x64
```
yarn build-platform --linux --skip-os-packages --release
```
This will produce an artifact under `{root}/target/opensearch-dashboards-{version}-linux-x64.tar.gz

### Linux ARM64
To build a release version for Linux x64
```
yarn build-platform --linux-arm --skip-os-packages --release
```
This will produce an artifact under `{root}/target/opensearch-dashboards-{version}-linux-arm64.tar.gz

### Linux RPM
`TODO`

### Linux DEB
`TODO`

### Windows
Currently not supported

### MacOS
Currently not supported

## Snapshot
`TODO`

