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

## Next steps

This plugin is best used in combination with [this prettier
configuration](https://github.com/mtth/prettier-typescript) and the following
convenience scripts:

+ `fix`: `prettier --write 'src/**/*.ts' 'test/**/*.ts' && npm run lint -- --fix`
+ `lint`: `eslint 'src/**/*.ts' 'test/**/*.ts'`

We also recommend enabling pre-commit hooks with `husky` and `lint-staged`. For
example, within your `package.json`:

```json
{
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged"
    }
  },
  "lint-staged": {
    "*.ts": [
      "prettier --write",
      "eslint --fix"
    ]
  }
}
```
