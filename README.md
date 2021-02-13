# ESLint plugin

Shared linting configuration.

## Quickstart

First, install ESLint and the plugin:

```sh
$ npm i -D eslint @mtth/eslint-plugin
```

Then reference this plugin in `.eslintrc.js`:

```js
module.exports = {
  plugins: ['@mtth'],
  extends: ['plugin:@mtth/typescript'],
  // Project-specific configuration...
};
```
