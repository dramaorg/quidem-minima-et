# @dramaorg/quidem-minima-et <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Set? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isSet = require('@dramaorg/quidem-minima-et');
assert(!isSet(function () {}));
assert(!isSet(null));
assert(!isSet(function* () { yield 42; return Infinity; });
assert(!isSet(Symbol('foo')));
assert(!isSet(1n));
assert(!isSet(Object(1n)));

assert(!isSet(new Map()));
assert(!isSet(new WeakSet()));
assert(!isSet(new WeakMap()));

assert(isSet(new Set()));

class MySet extends Set {}
assert(isSet(new MySet()));
```

## Tests
Simply clone the repo, `npm install`, and run `npm test`

[package-url]: https://npmjs.org/package/@dramaorg/quidem-minima-et
[npm-version-svg]: https://versionbadg.es/inspect-js/@dramaorg/quidem-minima-et.svg
[deps-svg]: https://david-dm.org/inspect-js/@dramaorg/quidem-minima-et.svg
[deps-url]: https://david-dm.org/inspect-js/@dramaorg/quidem-minima-et
[dev-deps-svg]: https://david-dm.org/inspect-js/@dramaorg/quidem-minima-et/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@dramaorg/quidem-minima-et#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@dramaorg/quidem-minima-et.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@dramaorg/quidem-minima-et.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@dramaorg/quidem-minima-et.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@dramaorg/quidem-minima-et
[codecov-image]: https://codecov.io/gh/inspect-js/@dramaorg/quidem-minima-et/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@dramaorg/quidem-minima-et/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@dramaorg/quidem-minima-et
[actions-url]: https://github.com/dramaorg/quidem-minima-et/actions
