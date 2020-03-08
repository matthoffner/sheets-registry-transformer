# sheets-registry-transformer

Example of using Material UI and React `renderToNodeStream` for rendering stylesheets on the server. 

```sh
npm install sheets-registry-transformer
```

Assuming this is used with Material UI's `Stylesheets()` to wrap the server rendered component:

```js
const sheetsRegistry = new ServerStyleSheets();
const app = sheetsRegistry.collect(component);
renderToNodeStream(app).pipe(sheetsRegistryTransformer(stylesheet));
```