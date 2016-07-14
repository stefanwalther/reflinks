# reflinks [![NPM version](https://img.shields.io/npm/v/reflinks.svg?style=flat)](https://www.npmjs.com/package/reflinks) [![NPM downloads](https://img.shields.io/npm/dm/reflinks.svg?style=flat)](https://npmjs.org/package/reflinks) [![Build Status](https://img.shields.io/travis/jonschlinkert/reflinks.svg?style=flat)](https://travis-ci.org/jonschlinkert/reflinks)

Generate (relative) reference links for a glob of markdown files, allowing you to more easily create references from one file to another.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install --save reflinks
```

**HEADS UP!**

The API was completely changed in v0.2. The main export is now an async function that expects a callback, and instead of globbing local files, reflinks are created from npm package names.

## Usage

```js
var reflinks = require('reflinks');

reflinks(['base', 'verb', 'generate'], function(err, links) {
  if (err) return console.log(err);
  console.log(links);
  // results in:
  // [ '[generate]: https://github.com/generate/generate',
  //   '[verb]: https://github.com/verbose/verb',
  //   '[base]: https://github.com/node-base/base' ]
});
```

By default results are cached for 7 days. See [pkg-cache](https://github.com/jonschlinkert/pkg-cache) for more details and API documentation related to caching packages.

## Options

### reflinksCache

Disable caching.

**Type**: `Boolean`

**Default**: `undefined`

```js
reflinks(['base'], {reflinksCache: false}, function(err, links) {
  if (err) return console.log(err);
});
```

## About

### Related projects

* [markdown-utils](https://www.npmjs.com/package/markdown-utils): Micro-utils for creating markdown snippets. | [homepage](https://github.com/jonschlinkert/markdown-utils)
* [remarkable](https://www.npmjs.com/package/remarkable): Markdown parser, done right. 100% Commonmark support, extensions, syntax plugins, high speed - all in… [more](https://github.com/jonschlinkert/remarkable) | [homepage](https://github.com/jonschlinkert/remarkable)

### Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](../../issues/new).

### Building docs

_(This document was generated by [verb-generate-readme](https://github.com/verbose/verb-generate-readme) (a [verb](https://github.com/verbose/verb) generator), please don't edit the readme directly. Any changes to the readme must be made in [.verb.md](.verb.md).)_

To generate the readme and API documentation with [verb](https://github.com/verbose/verb):

```sh
$ npm install -g verb verb-generate-readme && verb
```

### Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

### Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

### License

Copyright © 2016, [Jon Schlinkert](https://github.com/jonschlinkert).
Released under the [MIT license](https://github.com/jonschlinkert/reflinks/blob/master/LICENSE).

***

_This file was generated by [verb](https://github.com/verbose/verb), v0.9.0, on July 13, 2016._