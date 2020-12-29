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