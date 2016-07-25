# Force Webpack Error

Example repo that forces a module parse error in webpack to
showcase that webpack seems to treat this as a success.

1. `npm install`
2. cd `force-error`
3. `npm install`
4. `../node_modules/.bin/webpack --config ../webpack.config.js`

You will get the following output:

```ERROR in ./~/axios/package.json
Module parse failed: /home/ajcrites/blarg/force-err/node_modules/axios/package.json Unexpected token (2:9)
You may need an appropriate loader to handle this file type.
```

However, the built directory `lib` will still be created
even though it does not work properly. This error is written
to `stdout`, and `webpack` exits with 0 (success) status
