# @f1stnpm2/nobis-autem-voluptate <sup>[![Version Badge][npm-version-svg]][package-url]</sup>

[![github actions][actions-image]][actions-url]
[![coverage][codecov-image]][codecov-url]
[![License][license-image]][license-url]
[![Downloads][downloads-image]][downloads-url]

[![npm badge][npm-badge-png]][package-url]

Is this value a JS Set? This module works cross-realm/iframe, and despite ES6 @@toStringTag.

## Example

```js
var isSet = require('@f1stnpm2/nobis-autem-voluptate');
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

[package-url]: https://npmjs.org/package/@f1stnpm2/nobis-autem-voluptate
[npm-version-svg]: https://versionbadg.es/inspect-js/@f1stnpm2/nobis-autem-voluptate.svg
[deps-svg]: https://david-dm.org/inspect-js/@f1stnpm2/nobis-autem-voluptate.svg
[deps-url]: https://david-dm.org/inspect-js/@f1stnpm2/nobis-autem-voluptate
[dev-deps-svg]: https://david-dm.org/inspect-js/@f1stnpm2/nobis-autem-voluptate/dev-status.svg
[dev-deps-url]: https://david-dm.org/inspect-js/@f1stnpm2/nobis-autem-voluptate#info=devDependencies
[npm-badge-png]: https://nodei.co/npm/@f1stnpm2/nobis-autem-voluptate.png?downloads=true&stars=true
[license-image]: https://img.shields.io/npm/l/@f1stnpm2/nobis-autem-voluptate.svg
[license-url]: LICENSE
[downloads-image]: https://img.shields.io/npm/dm/@f1stnpm2/nobis-autem-voluptate.svg
[downloads-url]: https://npm-stat.com/charts.html?package=@f1stnpm2/nobis-autem-voluptate
[codecov-image]: https://codecov.io/gh/inspect-js/@f1stnpm2/nobis-autem-voluptate/branch/main/graphs/badge.svg
[codecov-url]: https://app.codecov.io/gh/inspect-js/@f1stnpm2/nobis-autem-voluptate/
[actions-image]: https://img.shields.io/endpoint?url=https://github-actions-badge-u3jn4tfpocch.runkit.sh/inspect-js/@f1stnpm2/nobis-autem-voluptate
[actions-url]: https://github.com/f1stnpm2/nobis-autem-voluptate/actions
