### Publishing

```
To publish new version there is possible (instead npm publish) use fully-automated command (npm version) to bump version, bump git tag and publish new npm package version in one command:

npm version patch // update patch version number 1.2.X (v1.2.3 to v1.2.4)
npm version minor // update minor version number  1.X.3 (v1.2.3 to v 1.3.0)
npm version major // update major version number  X.2.3 (v1.2.3 to v 2.0.0)
You can use --m "Commit message here" to customize auto-bump commit message.

More command options here: https://docs.npmjs.com/cli/version (i.e. --force)
```

[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

# podio-js [![Build Status](https://travis-ci.org/podio/podio-js.svg?branch=master)](https://travis-ci.org/podio/podio-js) [![Dependency Status](http://img.shields.io/gemnasium/podio/podio-js.svg?style=flat-square)](https://gemnasium.com/podio/podio-js) [![Coverage](http://img.shields.io/coveralls/podio/podio-js.svg?style=flat-square)](https://coveralls.io/r/podio/podio-js)

> Official Podio JavaScript SDK for Node and the browser

## Installation

```sh
$ npm install podio-js --save
```

## Usage

#### Node

```js
var Podio = require("podio-js").api;

var podio = new Podio({
  authType: "server",
  clientId: "id",
  clientSecret: "secret",
});
```

#### Express Middleware

Simple express middleware for storing the Podio token

```js
app.use(
  require("podio-js").middleware({
    clientId: "id",
    clientSecret: "secret",
  })
);
```

#### Browser

If you are using and AMD/CommonJS compatible module loader you can require the module:

```js
var PodioJS = require("podio-js");
```

If you are not using a loader, browserify `podio-js` like this:

```sh
$ npm install -g browserify

$ npm run bundle
```

and include `dist/podio-js.js` using a `<script>` tag.

## Documentation

You will find a detailed documentation at [http://podio.github.io/podio-js/](http://podio.github.io/podio-js/) and at [https://developers.podio.com/](https://developers.podio.com/)

## Tests

```sh
$ npm test
```
