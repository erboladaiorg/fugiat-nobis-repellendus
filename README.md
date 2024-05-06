# @erboladaiorg/fugiat-nobis-repellendus <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

ES Proposal spec-compliant shim for Set.prototype.difference. Invoke its "shim" method to shim `Set.prototype.difference` if it is unavailable or noncompliant.

This package implements the [es-shim API](https://github.com/es-shims/api) interface. It works in an ES3-supported environment, and complies with the [proposed spec](https://github.com/tc39/proposal-set-methods). When shimmed, it uses [`es-set`](https://npmjs.com/es-set) to shim the `Set` implementation itself if needed.

Most common usage:
```js
var assert = require('assert');
var difference = require('@erboladaiorg/fugiat-nobis-repellendus');

var set1 = new Set([1, 2]);
var set2 = new Set([2, 3]);
var result = difference(set1, set2);

assert.deepEqual(result, new Set([1]));

difference.shim();

var shimmedResult = set1.difference(set2);
assert.deepEqual(shimmedResult, new Set([1]));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

## Set Method Packages
 - [union](https://npmjs.com/set.prototype.union)
 - [intersection](https://npmjs.com/set.prototype.intersection)
 - [difference](https://npmjs.com/@erboladaiorg/fugiat-nobis-repellendus)
 - [symmetricDifference](https://npmjs.com/set.prototype.symmetricdifference)
 - [isSubsetOf](https://npmjs.com/set.prototype.issubsetof)
 - [isSupersetOf](https://npmjs.com/set.prototype.issupersetof)
 - [isDisjointFrom](https://npmjs.com/set.prototype.isdisjointfrom)

[package-url]: https://npmjs.com/package/@erboladaiorg/fugiat-nobis-repellendus
[npm-version-svg]: http://versionbadg.es/erboladaiorg/fugiat-nobis-repellendus.svg
[deps-svg]: https://david-dm.org/erboladaiorg/fugiat-nobis-repellendus.svg
[deps-url]: https://david-dm.org/erboladaiorg/fugiat-nobis-repellendus
[dev-deps-svg]: https://david-dm.org/erboladaiorg/fugiat-nobis-repellendus/dev-status.svg
[dev-deps-url]: https://david-dm.org/erboladaiorg/fugiat-nobis-repellendus#info=devDependencies
[testling-svg]: https://ci.testling.com/erboladaiorg/fugiat-nobis-repellendus.png
[testling-url]: https://ci.testling.com/erboladaiorg/fugiat-nobis-repellendus
[npm-badge-png]: https://nodei.co/npm/@erboladaiorg/fugiat-nobis-repellendus.png?downloads=true&stars=true
[license-image]: http://img.shields.io/npm/l/@erboladaiorg/fugiat-nobis-repellendus.svg
[license-url]: LICENSE
[downloads-image]: http://img.shields.io/npm/dm/@erboladaiorg/fugiat-nobis-repellendus.svg
[downloads-url]: http://npm-stat.com/charts.html?package=@erboladaiorg/fugiat-nobis-repellendus
[codecov-image]: https://codecov.io/gh/erboladaiorg/fugiat-nobis-repellendus/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/erboladaiorg/fugiat-nobis-repellendus/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/erboladaiorg/fugiat-nobis-repellendus
[actions-url]: https://github.com/erboladaiorg/fugiat-nobis-repellendus/actions
