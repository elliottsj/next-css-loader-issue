# next-css-loader-issue
Repro of an issue using next-css with Next.js v9.1.0

### Install

```
yarn
```

### Run

```
yarn dev
```

Observe the error:

```
yarn run v1.19.0
$ next
[ wait ]  starting the development server ...
[ info ]  waiting on http://localhost:3000 ...
[ ready ] compiled successfully - ready on http://localhost:3000
[ wait ]  compiling ...
[ ready ] compiled successfully - ready on http://localhost:3000
[ event ] build page: /
[ wait ]  compiling ...
[ error ] ./pages/index.css
ValidationError: Invalid options object. CSS Loader has been initialised using an options object that does not match the API schema.
 - options has an unknown property 'exportOnlyLocals'. These properties are valid:
   object { url?, import?, modules?, sourceMap?, importLoaders?, localsConvention?, onlyLocals? }
Could not find files for /index in .next/build-manifest.json
ModuleBuildError: Module build failed (from ./node_modules/extract-css-chunks-webpack-plugin/dist/loader.js):
ModuleBuildError: Module build failed (from ./node_modules/css-loader/dist/cjs.js):
ValidationError: Invalid options object. CSS Loader has been initialised using an options object that does not match the API schema.
 - options has an unknown property 'exportOnlyLocals'. These properties are valid:
   object { url?, import?, modules?, sourceMap?, importLoaders?, localsConvention?, onlyLocals? }
    at validate (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/css-loader/node_modules/schema-utils/dist/validate.js:50:11)
    at Object.loader (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/css-loader/dist/index.js:34:28)
    at runLoaders (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/webpack/lib/NormalModule.js:313:20)
    at /Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/loader-runner/lib/LoaderRunner.js:367:11
    at /Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/loader-runner/lib/LoaderRunner.js:233:18
    at runSyncOrAsync (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/loader-runner/lib/LoaderRunner.js:143:3)
    at iterateNormalLoaders (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/loader-runner/lib/LoaderRunner.js:232:2)
    at Array.<anonymous> (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/loader-runner/lib/LoaderRunner.js:205:4)
    at Storage.finished (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/enhanced-resolve/lib/CachedInputFileSystem.js:55:16)
    at provider (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/enhanced-resolve/lib/CachedInputFileSystem.js:91:9)
    at /Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/graceful-fs/graceful-fs.js:115:16
    at FSReqWrap.readFileAfterClose [as oncomplete] (internal/fs/read_file_context.js:53:3)
    at runLoaders (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/webpack/lib/NormalModule.js:313:20)
    at /Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/loader-runner/lib/LoaderRunner.js:367:11
    at /Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/loader-runner/lib/LoaderRunner.js:182:20
    at context.callback (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/loader-runner/lib/LoaderRunner.js:111:13)
    at /Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/extract-css-chunks-webpack-plugin/dist/loader.js:113:20
    at compile (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/webpack/lib/Compiler.js:343:11)
    at hooks.afterCompile.callAsync.err (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/webpack/lib/Compiler.js:671:15)
    at AsyncSeriesHook.eval [as callAsync] (eval at create (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/tapable/lib/HookCodeFactory.js:33:10), <anonymous>:24:1)
    at AsyncSeriesHook.lazyCompileHook (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/tapable/lib/Hook.js:154:20)
    at compilation.seal.err (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/webpack/lib/Compiler.js:668:31)
    at AsyncSeriesHook.eval [as callAsync] (eval at create (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/tapable/lib/HookCodeFactory.js:33:10), <anonymous>:6:1)
    at AsyncSeriesHook.lazyCompileHook (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/tapable/lib/Hook.js:154:20)
    at hooks.optimizeAssets.callAsync.err (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/webpack/lib/Compilation.js:1385:35)
    at AsyncSeriesHook.eval [as callAsync] (eval at create (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/tapable/lib/HookCodeFactory.js:33:10), <anonymous>:6:1)
    at AsyncSeriesHook.lazyCompileHook (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/tapable/lib/Hook.js:154:20)
    at hooks.optimizeChunkAssets.callAsync.err (/Users/spencerelliott/Dev/elliottsj/next-css-loader-issue/node_modules/webpack/lib/Compilation.js:1376:32)
```
