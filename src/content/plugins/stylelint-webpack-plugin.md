---
title: StylelintWebpackPlugin
source: https://raw.githubusercontent.com/webpack-contrib/stylelint-webpack-plugin/master/README.md
edit: https://github.com/webpack-contrib/stylelint-webpack-plugin/edit/master/README.md
repo: https://github.com/webpack-contrib/stylelint-webpack-plugin
---


[![npm][npm]][npm-url]
[![node][node]][node-url]
[![deps][deps]][deps-url]
[![tests][tests]][tests-url]
[![coverage][cover]][cover-url]
[![chat][chat]][chat-url]
[![size][size]][size-url]



> A Stylelint plugin for webpack

## Install {#install}

```bash
npm install stylelint-webpack-plugin --save-dev
```

**Note**: You also need to install `stylelint` from npm, if you haven't already:

```bash
npm install stylelint --save-dev
```

## Usage {#usage}

In your webpack configuration:

```js
const StylelintPlugin = require('stylelint-webpack-plugin');

module.exports = {
  // ...
  plugins: [new StylelintPlugin(options)],
  // ...
};
```

## Options {#options}

See [stylelint's options](http://stylelint.io/user-guide/node-api/#options) for the complete list of options available. These options are passed through to the `stylelint` directly.

### `configFile` {#configfile}

- Type: `String`
- Default: `undefined`

Specify the config file location to be used by `stylelint`.

**Note:** By default this is [handled by `stylelint`](http://stylelint.io/user-guide/configuration/).

### `context` {#context}

- Type: `String`
- Default: `compiler.context`

A string indicating the root of your files.

### `files` {#files}

- Type: `String|Array[String]`
- Default: `'**/*.s?(a|c)ss'`

Specify the glob pattern for finding files. Must be relative to `options.context`.

### `fix` {#fix}

- Type: `Boolean`
- Default: `false`

If `true`, `stylelint` will fix as many errors as possible. The fixes are made to the actual source files. All unfixed errors will be reported. See [Autofixing errors](https://stylelint.io/user-guide/cli#autofixing-errors) docs.

### `formatter` {#formatter}

- Type: `String|Function`
- Default: `'string'`

Specify the formatter that you would like to use to format your results. See [formatter option](https://stylelint.io/user-guide/node-api#formatter).

### `lintDirtyModulesOnly` {#lintdirtymodulesonly}

- Type: `Boolean`
- Default: `false`

Lint only changed files, skip lint on start.

### `stylelintPath` {#stylelintpath}

- Type: `String`
- Default: `stylelint`

Path to `stylelint` instance that will be used for linting.

### Errors and Warning {#errors-and-warning}

**By default the plugin will auto adjust error reporting depending on stylelint errors/warnings counts.**
You can still force this behavior by using `emitError` **or** `emitWarning` options:

#### `emitError` {#emiterror}

- Type: `Boolean`
- Default: `false`

Will always return errors, if set to `true`.

#### `emitWarning` {#emitwarning}

- Type: `Boolean`
- Default: `false`

Will always return warnings, if set to `true`.

#### `failOnError` {#failonerror}

- Type: `Boolean`
- Default: `false`

Will cause the module build to fail if there are any errors, if set to `true`.

#### `failOnWarning` {#failonwarning}

- Type: `Boolean`
- Default: `false`

Will cause the module build to fail if there are any warnings, if set to `true`.

#### `quiet` {#quiet}

- Type: `Boolean`
- Default: `false`

Will process and report errors only and ignore warnings, if set to `true`.

## Changelog {#changelog}

[Changelog](https://github.com/webpack-contrib/stylelint-webpack-plugin/blob/master/CHANGELOG.md)

## License {#license}

[MIT](https://github.com/webpack-contrib/stylelint-webpack-plugin/blob/master/LICENSE)

[npm]: https://img.shields.io/npm/v/stylelint-webpack-plugin.svg
[npm-url]: https://npmjs.com/package/stylelint-webpack-plugin
[node]: https://img.shields.io/node/v/stylelint-webpack-plugin.svg
[node-url]: https://nodejs.org/
[deps]: https://david-dm.org/webpack-contrib/stylelint-webpack-plugin.svg
[deps-url]: https://david-dm.org/webpack-contrib/stylelint-webpack-plugin
[tests]: https://github.com/webpack-contrib/stylelint-webpack-plugin/workflows/stylelint-webpack-plugin/badge.svg
[tests-url]: https://github.com/webpack-contrib/stylelint-webpack-plugin/actions
[cover]: https://codecov.io/gh/webpack-contrib/stylelint-webpack-plugin/branch/master/graph/badge.svg
[cover-url]: https://codecov.io/gh/webpack-contrib/stylelint-webpack-plugin
[chat]: https://badges.gitter.im/webpack/webpack.svg
[chat-url]: https://gitter.im/webpack/webpack
[size]: https://packagephobia.now.sh/badge?p=stylelint-webpack-plugin
[size-url]: https://packagephobia.now.sh/result?p=stylelint-webpack-plugin
