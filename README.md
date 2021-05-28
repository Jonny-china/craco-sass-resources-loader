# Craco sass-resources-loader

> Modify with [tilap/craco-sass-resources-loader](https://github.com/tilap/craco-sass-resources-loader)

[![MIT License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)

This is a [craco](https://github.com/sharegate/craco) plugin to add [sass-resources-loader](https://www.npmjs.com/package/sass-resources-loader) with [create-react-app](https://facebook.github.io/create-react-app/) version >= 2.

## Installation

```bash
$ yarn add -D @jonny1994/craco-sass-resources-loader

# OR

$ npm install @jonny1994/craco-sass-resources-loader --save-dev
```

## Usage

`craco-sass-resources-loader` expect a `resources` option containing a string or an array of
string pointing the scss files your want to load before any scss/sass file.

```js
const sassResourcesLoader = require('@jonny1994/craco-sass-resources-loader');

module.exports = {
  plugins: [
    {
      plugin: sassResourcesLoader,
      options: {
        hoistUseStatements: false,
        resources: './src/my-config-theme.scss',
      },
    },
  ],
}
```

You can load multiple scss resources files too:

```js
const sassResourcesLoader = require('craco-sass-resources-loader');

module.exports = {
  plugins: [
    {
      plugin: sassResourcesLoader,
      options: {
        resources: [
          './src/my-config-theme.scss',
          './src/my-other-config-theme.scss'
        ],
      },
    },
  ],
}
```
