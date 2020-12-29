# setup
```
$ mkdir hard-svelte && cd hard-svelte
$ npm init -y
$ npm install --save svelte
$ npm install --save-dev @babel/core @babel/preset-env @babel/preset-typescript @tsconfig/svelte@ @wessberg/rollup-plugin-ts rollup rollup-plugin-node-resolve rollup-plugin-svelte svelte-preprocess typescript svelte-check rollup-plugin-terser rollup-plugin-analyzer es-check bundlesize autoprefixer postcss postcss-cli
```

# serve
`dist/index.html`に以下のHTMLを配置

```
<html>
  <body>
    <div id="root"></div>
    <script src="index.js"></script>
  </body>
</html>
```

```
$ open dist/index.html
```

# verify
dist に吐かれた生成物のサイズを確認
```
$ la # ls -alh
total 144
drwxr-xr-x   5 s_harada  staff   160B 12 29 16:21 .
drwxr-xr-x  14 s_harada  staff   448B 12 29 16:13 ..
-rw-r--r--@  1 s_harada  staff    96B 12 29 16:21 index.html
-rw-r--r--   1 s_harada  staff   3.1K 12 29 16:14 index.js
-rw-r--r--   1 s_harada  staff    61K 12 29 16:14 index.js.map
```

`es-check`を使って、生成物が es5 (IE で動く水準) になっているか確認
```
$ npx es-check es5 ./dist/index.js
ES-Check: there were no ES version matching errors!  🎉
```

`svelte-check`を実行
```
$ npx svelte-check

Loading svelte-check in workspace: /Users/s_harada/Projects/github/hard-svelte
Getting Svelte diagnostics...
====================================

====================================
svelte-check found 0 errors, 0 warnings and 0 hints
```

# analyze
ビルドサイズの構成要素を検証
```
$ npm run analyze
```
