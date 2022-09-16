### OSD-PM Package Developer guide

### What is the intent of this package

* @osdpm package is a tool built to identify and build the package dependency graph and bundle all the files/modules inside the project into single js file. 
* @osdpm tool enables us to share static dependencies/packages between OpenSearch Dashboards and OpenSearch Dashboards plugins. 
* It also enables packages to have their own dependencies and build scripts which can be run using @osdpm tool.

### How packages depend on one another?

``` npm link ``` 

This is used to share the package between repo's without publishing the packaged bundle to npm registry and just by symlinking the package to the code in other repo.  This will just push the symlinked library/package bundle into node modules in the local user root space and just pulling it down when symlinked from other repo.

```
"@osd/i18n": "link:packages/osd-i18n"
```

Here `packages/osd-i18n` is the relative path to the `osd-i18n` package inside OpenSearch Dashboard repo.

### OSDPM commands 

* `bootstrap`
  - Install dependencies and crosslink projects
  - Topologically batches the project by its workspace
  - Parallelize Batches where all the packages within a batch are build in parallel before going to the next batch of projects in topological order.
  - Read `yarn.lock` file
  - Validate all the dependencies
  - Link project executables
  - Calculate checksums for all projects in the workspace
  - Cache the bootstrapped builds
 
 ```
 yarn osd bootstrap
 ```

Some other OSD-PM commands are - 
* `clean`
  - Remove the node_modules and target directories from all projects.
* `run`
  - Run script defined in package.json in each package that contains that script.

 ```
yarn osd run build
 ```

* `watch`
  - Command that traverses through list of available projects/packages that have `osd:watch` script in their
 package.json files, groups them into topology aware batches and then processes theses batches one by one
 running `osd:watch` scripts in parallel within the same batch.

```
yarn osd watch
```



### `watch` @osdpm build

```
yarn osd watch --include @osd/pm
```

```js
@osd/pm <s> [webpack.Progress] 68% building 635/646 modules 11 active /home/ubuntu/OpenSearch-Dashboards/node_modules/is-number/index.js
@osd/pm <s> [webpack.Progress] 68% building 635/647 modules 12 active /home/ubuntu/OpenSearch-Dashboards/node_modules/repeat-string/index.js
@osd/pm <s> [webpack.Progress] 68% building 635/648 modules 13 active /home/ubuntu/OpenSearch-Dashboards/node_modules/cpy/node_modules/to-regex-range/index.js
@osd/pm <s> [webpack.Progress] 68% building 635/649 modules 14 active /home/ubuntu/OpenSearch-Dashboards/node_modules/ret/lib/util.js
.........
@osd/pm <s> [webpack.Progress] 70% building 713/713 modules 0 active 
@osd/pm <s> [webpack.Progress] 69% building 713/714 modules 1 active /home/ubuntu/OpenSearch-Dashboards/node_modules/isarray/index.js
@osd/pm <s> [webpack.Progress] 70% building 714/714 modules 0 active 
@osd/pm <s> [webpack.Progress] 70% building 714/714 modules 0 active 
@osd/pm <s> [webpack.Progress] 70% finish module graph
@osd/pm <s> [webpack.Progress] 70% finish module graph FlagDependencyExportsPlugin
@osd/pm <s> [webpack.Progress] 70% sealing
@osd/pm <s> [webpack.Progress] 70% sealing WarnCaseSensitiveModulesPlugin
@osd/pm <s> [webpack.Progress] 72% basic dependencies optimization
@osd/pm <s> [webpack.Progress] 72% dependencies optimization
@osd/pm <s> [webpack.Progress] 73% advanced dependencies optimization
@osd/pm <s> [webpack.Progress] 73% after dependencies optimization
@osd/pm <s> [webpack.Progress] 71% chunk graph
@osd/pm <s> [webpack.Progress] 71% after chunk graph
@osd/pm <s> [webpack.Progress] 71% after chunk graph WebAssemblyModulesPlugin
@osd/pm <s> [webpack.Progress] 74% optimizing
@osd/pm <s> [webpack.Progress] 74% basic module optimization
@osd/pm <s> [webpack.Progress] 75% module optimization
@osd/pm <s> [webpack.Progress] 75% advanced module optimization
@osd/pm <s> [webpack.Progress] 76% after module optimization
@osd/pm <s> [webpack.Progress] 76% basic chunk optimization
@osd/pm <s> [webpack.Progress] 76% basic chunk optimization EnsureChunkConditionsPlugin
@osd/pm <s> [webpack.Progress] 76% basic chunk optimization RemoveParentModulesPlugin
@osd/pm <s> [webpack.Progress] 76% basic chunk optimization RemoveEmptyChunksPlugin
@osd/pm <s> [webpack.Progress] 76% basic chunk optimization MergeDuplicateChunksPlugin
@osd/pm <s> [webpack.Progress] 77% chunk optimization
@osd/pm <s> [webpack.Progress] 77% advanced chunk optimization
@osd/pm <s> [webpack.Progress] 77% advanced chunk optimization SplitChunksPlugin
@osd/pm <s> [webpack.Progress] 77% advanced chunk optimization RemoveEmptyChunksPlugin
@osd/pm <s> [webpack.Progress] 77% after chunk optimization
@osd/pm <s> [webpack.Progress] 78% module and chunk tree optimization
@osd/pm <s> [webpack.Progress] 78% after module and chunk tree optimization
@osd/pm <s> [webpack.Progress] 79% basic chunk modules optimization
@osd/pm <s> [webpack.Progress] 80% chunk modules optimization
@osd/pm <s> [webpack.Progress] 80% advanced chunk modules optimization
@osd/pm <s> [webpack.Progress] 81% after chunk modules optimization
@osd/pm <s> [webpack.Progress] 81% module reviving
@osd/pm <s> [webpack.Progress] 81% module reviving RecordIdsPlugin
@osd/pm <s> [webpack.Progress] 82% module order optimization
@osd/pm <s> [webpack.Progress] 82% advanced module order optimization
@osd/pm <s> [webpack.Progress] 83% before module ids
@osd/pm <s> [webpack.Progress] 83% module ids
@osd/pm <s> [webpack.Progress] 84% module id optimization
@osd/pm <s> [webpack.Progress] 84% module id optimization
@osd/pm <s> [webpack.Progress] 85% chunk reviving
@osd/pm <s> [webpack.Progress] 85% chunk reviving RecordIdsPlugin
@osd/pm <s> [webpack.Progress] 85% chunk order optimization
@osd/pm <s> [webpack.Progress] 85% chunk order optimization NaturalChunkOrderPlugin
@osd/pm <s> [webpack.Progress] 86% before chunk ids
@osd/pm <s> [webpack.Progress] 86% chunk id optimization
@osd/pm <s> [webpack.Progress] 87% after chunk id optimization
@osd/pm <s> [webpack.Progress] 87% record modules
@osd/pm <s> [webpack.Progress] 87% record modules RecordIdsPlugin
@osd/pm <s> [webpack.Progress] 87% record chunks
@osd/pm <s> [webpack.Progress] 87% record chunks RecordIdsPlugin
@osd/pm <s> [webpack.Progress] 88% hashing
@osd/pm <s> [webpack.Progress] 88% after hashing
@osd/pm <s> [webpack.Progress] 89% record hash
@osd/pm <s> [webpack.Progress] 89% module assets processing
@osd/pm <s> [webpack.Progress] 90% chunk assets processing
@osd/pm <s> [webpack.Progress] 90% additional chunk assets processing
@osd/pm <s> [webpack.Progress] 91% recording
@osd/pm <s> [webpack.Progress] 92% additional asset processing
@osd/pm <s> [webpack.Progress] 92% chunk asset optimization
@osd/pm <s> [webpack.Progress] 93% after chunk asset optimization
@osd/pm <s> [webpack.Progress] 93% asset optimization
@osd/pm <s> [webpack.Progress] 94% after asset optimization
@osd/pm <s> [webpack.Progress] 94% after seal
@osd/pm <s> [webpack.Progress] 95% emitting
@osd/pm <s> [webpack.Progress] 98% after emitting
@osd/pm <s> [webpack.Progress] 100% 
@osd/pm Hash: 8a4ed7a022c7e06630e2
@osd/pm Version: webpack 4.46.0
@osd/pm Time: 1968ms
@osd/pm Built at: 08/19/2022 9:29:52 PM
@osd/pm    Asset     Size  Chunks             Chunk Names
@osd/pm index.js  2.3 MiB       0  [emitted]  index
@osd/pm Entrypoint index = index.js
@osd/pm   [0] ./src/index.ts 1.34 KiB {0} [built]
@osd/pm   [1] ./src/cli.ts 3.79 KiB {0} [built]
@osd/pm   [2] /home/ubuntu/OpenSearch-Dashboards/node_modules/dedent/dist/dedent.js 1.35 KiB {0} [built]
@osd/pm   [3] ./node_modules/getopts/index.cjs 4.44 KiB {0} [built]
@osd/pm   [4] external "path" 42 bytes {0} [built]
@osd/pm   [5] ../osd-dev-utils/target/tooling_log/index.js 2.23 KiB {0} [built]
@osd/pm [112] external "util" 42 bytes {0} [built]
@osd/pm [128] ./src/commands/index.ts 1.35 KiB {0} [built]
@osd/pm [131] ./src/utils/fs.ts 3.36 KiB {0} [built]
@osd/pm [134] external "fs" 42 bytes {0} [built]
@osd/pm [146] ./src/utils/projects.ts 6.6 KiB {0} [built]
@osd/pm [164] ./src/utils/project.ts 8.7 KiB {0} [built]
@osd/pm [279] ./src/utils/workspaces.ts 3.11 KiB {0} [built]
@osd/pm [280] ./src/config.ts 2.6 KiB {0} [built]
@osd/pm [508] ./src/production/index.ts 1.14 KiB {0} [built]
@osd/pm     + 699 hidden modules

 ...........
@osd/pm  @ /home/ubuntu/OpenSearch-Dashboards/node_modules/validate-npm-package-license/node_modules/spdx-expression-parse/index.js
@osd/pm  @ /home/ubuntu/OpenSearch-Dashboards/node_modules/validate-npm-package-license/index.js
@osd/pm  @ /home/ubuntu/OpenSearch-Dashboards/node_modules/normalize-package-data/lib/fixer.js
@osd/pm  @ /home/ubuntu/OpenSearch-Dashboards/node_modules/normalize-package-data/lib/normalize.js
@osd/pm  @ /home/ubuntu/OpenSearch-Dashboards/node_modules/read-pkg/index.js
@osd/pm  @ ./src/utils/package_json.ts
@osd/pm  @ ./src/utils/workspaces.ts
@osd/pm  @ ./src/index.ts
 succ [@osd/pm] Initial build completed (webpack).
```


### Lerna

Tool for managing js projects with multiple packages.

Using lerna we can run scripts across the packages within a single repo.

```
lerna run test --scope={@package_id}
```

### yarn workspace

- Used to setup project like a monorepo method.
- Within a workspace, we can share code and share dependencies.
- There will be one `node_modules` in the whole workspace, every single project will not have its own `node_module` created when installed dependencies.
- There will be a project in a workspace with `package.json` which will define `workspaces` including list of packages which will be part of the workspace. 
- Inside packages specific manifest file, we need to define other package dependency and import it in the `index` file. 
- When a new dependency is added/installed inside a package, it gets added directly in the root folder `node_modules` folder instead of creating a separate `node_module` inside every package. So there will be one copy of all the dependencies inside root which will be shared among other packages.

```json
{
    "private": true,
    "workspaces": ["packages/osd-pm", "packages/osd-optimizer"]
}
```


### How does dependency tree is created?

* Webpack config file is responsible for bundling all of the modules in a package, transform some of the files if required such as css, svg's and transpile some of the js code (new js to old js compatible with old browsers) and intelligently bundle all of them by creating dependency tree graph of the modules. 
 * Should know the entry point of the file. This is configured in the `webpack.config` file by pointing to `index.js` file. `index.js` file is the starting point where all the modules are exported and webpack reads it from there. 
 * It examines all of the `import` and `require` statements and creates a dependency graph.
 * Should know if the modules need to be transformed using loaders. `module.rules` will capture all the loaders related information. Ex: Loaders to transform svg's, css files
 * Starts creating a bundle and place the bundle in one place - `dist` folder with file name `dist/index.js`

 ```js
 module.exports = {
  mode: 'none',
  entry: {
    index: './src/index.ts',
  },
  target: 'node',
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: '[name].js',
    libraryTarget: 'commonjs2',
  },
  module: {
    rules: [
      {
        test: /\.ts$/,
        use: [
          {
            loader: 'babel-loader',
          },
        ],
        exclude: /node_modules/,
      },
       ],
  },
  };
```


### Loaders vs WebPack Plugins

* Currently in OSD-PM webpack config we are using loaders to bundle the modules along with transforming the files and including them in the big bundler index.js file. All this is done before bundler gets generated. 
* But with plugins, we can transform the files (certain tasks) after bundle has been created. - Less restrictive forms of loaders

### What is Babel

Babel allows us to use new JS and at the same time not break user's browser. It transpiles new fancy javascript features to old js code which is mostly supported on most of the browsers which renders the html javascript code.


### `config.ts` in osdpm

 * Returns all the paths where plugins are located
 * The array list of paths also include plugin functional tests, interpreter functional tests, examples folder. 
 * We can configure to include `OpenSearchDashboardsPlugins`. If enabled, all the plugins and packages path will be included in the array of paths.



### `link_project_executables.ts`
  * This class takes project graph as its input. The job of this class is to go through each project's dependencies and manually linking the executables if it is defined. Before linking the executables, it make sure if the bin exists or else it will ignore it. 
  * Currently in OSD,  this is not done by `yarn`. Instead `@osdpm` tool manually does it by walking through each propject dependencies. 
