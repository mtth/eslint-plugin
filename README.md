# ESLint plugin

Shared linting configuration.

## Quickstart

First, install ESLint and this plugin:

```sh
$ npm i -D eslint @mtth/eslint-plugin
```

Then reference this plugin in `.eslintrc.js`:

```js
module.exports = {
  plugins: ['@mtth'],
  extends: ['plugin:@mtth/typescript'], // One of the configurations below.
  // Project-specific configuration...
};
```

## Configurations

+ `typescript`, defaults for a TypeScript project. The corresponding parser is
  included in the plugin.
