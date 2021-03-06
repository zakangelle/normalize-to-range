# normalize-to-range

Normalize an array of numbers or object property values to a specified range.

[![Circle CI](https://circleci.com/gh/zakangelle/normalize-to-range/tree/master.svg?style=shield)](https://circleci.com/gh/zakangelle/normalize-to-range/tree/master) [![Coverage Status](https://img.shields.io/coveralls/zakangelle/normalize-to-range.svg)](https://coveralls.io/github/zakangelle/normalize-to-range?branch=master)

## Installation

```
$ npm install normalize-to-range
```

## Usage

```js
import normalize from 'normalize-to-range';
```

Array of numbers:

```js
normalize([0, 1, 7, 9, 10], 0, 300);
// [0, 30, 210, 270, 300]
```

Array of objects:

```js
normalize([{ height: 12 }, { height: 40 }], 0, 1000, 'height');
// [{ height: 300 }, { height: 1000 }]
```

By default normalizes between 0 and 1:

```js
normalize([0, 1, 6, 10]);
// [0, 0.1, 0.6, 1]
```

## Standalone

Generate a standalone build in `dist` (for use with `<script>` tags and AMD module loaders):

```sh
$ npm run build:standalone
```

## Test
Tests are done with [tape](https://github.com/substack/tape) by running:

```
$ npm test
```

## License

MIT
