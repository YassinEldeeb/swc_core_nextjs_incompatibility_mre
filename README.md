# How to reproduce locally?

```sh
yarn install
yarn build
```

See logs. You'd see something like this:
```sh
yassineldeeb@192 swc-plugi-issue-reporduction % yarn build
yarn run v1.22.19
$ next build
 ✓ Linting and checking validity of types    
   Creating an optimized production build  ...thread '<unnamed>' panicked at 'called `Result::unwrap()` on an `Err` value: LayoutError', /home/runner/.cargo/registry/src/github.com-1ecc6299db9ec823/rkyv-0.7.41/src/impls/core/mod.rs:266:67
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
thread '<unnamed>' panicked at /Users/geist/.cargo/registry/src/index.crates.io-6f17d22bba15001f/swc-0.266.26/src/plugin.rs:162:14:
failed to invoke plugin: failed to invoke plugin on 'Some("/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/next/dist/pages/_document.js")'

Caused by:
    0: failed to invoke `/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm` as js transform plugin at /Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm
    1: RuntimeError: unreachable
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
thread 'thread '<unnamed><unnamed>' panicked at '' panicked at 'called `Result::unwrap()` on an `Err` value: LayoutError', called `Result::unwrap()` on an `Err` value: LayoutError', /home/runner/.cargo/registry/src/github.com-1ecc6299db9ec823/rkyv-0.7.41/src/impls/core/mod.rs/home/runner/.cargo/registry/src/github.com-1ecc6299db9ec823/rkyv-0.7.41/src/impls/core/mod.rs:266::26667:
67note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace

note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
thread '<unnamed>' panicked at /Users/geist/.cargo/registry/src/index.crates.io-6f17d22bba15001f/swc-0.266.26/src/plugin.rs:162:14:
failed to invoke plugin: failed to invoke plugin on 'Some("/Users/yassineldeeb/development/swc-plugi-issue-reporduction/pages/index.tsx")'

Caused by:
    0: failed to invoke `/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm` as js transform plugin at /Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm
    1: RuntimeError: unreachable
thread '<unnamed>' panicked at /Users/geist/.cargo/registry/src/index.crates.io-6f17d22bba15001f/swc-0.266.26/src/plugin.rs:162:14:
failed to invoke plugin: failed to invoke plugin on 'Some("/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/next/dist/pages/_error.js")'

Caused by:
    0: failed to invoke `/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm` as js transform plugin at /Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm
    1: RuntimeError: unreachable
Failed to compile.

./node_modules/next/dist/pages/_document.js
Error: failed to process failed to invoke plugin: failed to invoke plugin on 'Some("/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/next/dist/pages/_document.js")'

Caused by:
    0: failed to invoke `/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm` as js transform plugin at /Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm
    1: RuntimeError: unreachable

./node_modules/next/dist/pages/_error.js
Error: failed to process failed to invoke plugin: failed to invoke plugin on 'Some("/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/next/dist/pages/_error.js")'

Caused by:
    0: failed to invoke `/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm` as js transform plugin at /Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm
    1: RuntimeError: unreachable

Import trace for requested module:
./node_modules/next/dist/pages/_error.js

./pages/index.tsx
Error: failed to process failed to invoke plugin: failed to invoke plugin on 'Some("/Users/yassineldeeb/development/swc-plugi-issue-reporduction/pages/index.tsx")'

Caused by:
    0: failed to invoke `/Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm` as js transform plugin at /Users/yassineldeeb/development/swc-plugi-issue-reporduction/node_modules/@graphql-codegen/client-preset-swc-plugin/swc_plugin.wasm
    1: RuntimeError: unreachable

Import trace for requested module:
./pages/index.tsx


> Build failed because of webpack errors
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```