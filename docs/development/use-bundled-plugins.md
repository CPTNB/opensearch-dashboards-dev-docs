# Using bundled plugins in local development

## You want a quick way to add the security plugin to your local env

### 1. Start an instance of OpenSearch that already includes the security plugin

By default, we generally develop against a "minimal" version of OpenSearch, with no external plugins installed (such as when [running `yarn opensearch snapshot`](https://github.com/opensearch-project/OpenSearch-Dashboards/blob/main/DEVELOPER_GUIDE.md#run-opensearch)). This is great to make sure we understand the basic behavior of the core app. But that's not how most users install or run OpenSearch - they generally use all the bundled "default" plugins, of which [`security`](https://github.com/opensearch-project/security) is probably the most important.

#### Install and run a "full" version of OpenSearch via tarball

_(Do this on the same machine where you're developing on OpenSearch Dashboards - these examples assume you're using [an Ubuntu dev environment](https://quip-amazon.com/umanA1aLbFsw/Setup-Ubuntu-Machine-for-OpenSearch-devtest))_

1. Make/navigate to a directory where you want to store/run OpenSearch tarballs
2. Download the latest version of the OpenSearch tarball
  `curl https://artifacts.opensearch.org/releases/bundle/opensearch/{VERSION_NUMBER}/opensearch-{VERSION_NUMBER}-linux-x64.tar.gz --output opensearch-{VERSION_NUMBER}-linux-x64.tar.gz`
  for example, if you want version `2.1.0`,
  `curl https://artifacts.opensearch.org/releases/bundle/opensearch/2.1.0/opensearch-2.1.0-linux-x64.tar.gz --output opensearch-2.1.0-linux-x64.tar.gz`
3. Unzip it: `tar -zxf opensearch-{VERSION_NUMBER}-linux-x64.tar.gz`
4. `cd` inside and run `./opensearch-tar-install.sh ` (this is the only step necessary to subsequently restart the service)

_(The above is a slightly streamlined version of [the official tarball installation documentation](https://opensearch.org/docs/latest/opensearch/install/tar/))_

### 2. Install the OpenSearch Dashboards security plugin

Within the `plugins` directory of your local `OpenSearch-Dashboards` repo, clone the latest version of the security dashboards plugin: `git clone git@github.com:opensearch-project/security-dashboards-plugin.git`

### 3. Update the version strings to pass the version match test

In `plugins/security-dashboards-plugin/opensearch_dashboards.json` update the `opensearchDashboardsVersion` and  `version` strings to match the current version of OpenSearch Dashboards as defined in `package.json`.

### 4. Bootstrap

Run `yarn osd bootstrap` to build the newly installed plugin.

### 5. Update your config with minimal settings

The security plugin requires some config values to be set to start properly. Add the following configurations to `config/opensearch_dashboards.yml`:

```yml
csp.warnLegacyBrowsers: false
opensearch.ignoreVersionMismatch: true

opensearch.hosts: [https://localhost:9200]
opensearch.ssl.verificationMode: none
opensearch.username: kibanaserver
opensearch.password: kibanaserver
opensearch.requestHeadersWhitelist: [authorization, securitytenant]

opensearch_security.multitenancy.enabled: true
opensearch_security.multitenancy.tenants.preferred: [Private, Global]
opensearch_security.readonly_mode.roles: [kibana_read_only]
# Use this setting if you are running opensearch-dashboards without https
opensearch_security.cookie.secure: false
```

### 6. Start OpenSearch Dashboards

Now you can start normally: `yarn start`

### Notes and gotchas

1. The `/plugins` directory is gitignored, and may be cleared by various operations, in which case you'll need to repeat steps 2-4
2. It's annoying to constantly copy/paste the configurations required for the security dashboards plugin to start. One workaround is to `git stash` the changes and `git stash apply` it whenever you re-add the plugin.
