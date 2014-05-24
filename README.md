# koa-combo
[KoaJS](https://github.com/koajs/koa) middleware for combining static files at serverside to reduce the number of http requests.

### Installation
```shell
$ npm install koa-combo
```

### Usage
Enabling combo is as simple as following

```js
var koa = require('koa'),
  app = koa(),
  combo = require('koa-combo');

app.use(combo);
```

To access your combined static files, use the query string pattern `combo=path-of-file-1,path-of-file-2,path-of-file-3,...`.

### Example
Run `example.js` in harmony mode. **Ensure your node supports ES6 harmony mode**.

```shell
$ node --harmony example.js
```

Then visit `http://localhost:3000/?combo=example-parts/part1.js,example-parts/part2.js`, you will get the combined version of `example-parts/part1.js` and `example-parts/part2.js`. Files are concatenated by the given order in query string.

### License
MIT