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
warn  - You have enabled experimental feature (swcPlugins) in next.config.js.
warn  - Experimental features are not covered by semver, and may cause unexpected or broken application behavior. Use at your own risk.

info  - Linting and checking validity of types  
info  - Creating an optimized production build  
info  - Compiled successfully
info  - Collecting page data  
info  - Generating static pages (3/3)
info  - Finalizing page optimization  

Route (pages)                              Size     First Load JS
┌ ○ /                                      27.9 kB         102 kB
├   /_app                                  0 B              74 kB
└ ○ /404                                   182 B          74.2 kB
+ First Load JS shared by all              74 kB
  ├ chunks/framework-cda2f1305c3d9424.js   45.2 kB
  ├ chunks/main-17a9a24315ee9390.js        27.8 kB
  ├ chunks/pages/_app-b988dbfd45b396af.js  273 B
  └ chunks/webpack-4e7214a60fad8e88.js     712 B

○  (Static)  automatically rendered as static HTML (uses no initial props)

✨  Done in 9.96s.
```