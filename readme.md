# semver-regex

> Regular expression for matching [semver](https://github.com/npm/node-semver) versions

## Install

```
$ npm install semver-regex
```

## Usage

```js
import semverRegex from 'semver-regex';

semverRegex().test('v1.0.0');
//=> true

semverRegex().test('1.2.3-alpha.10.beta.0+build.unicorn.rainbow');
//=> true

semverRegex().exec('unicorn 1.0.0 rainbow')[0];
//=> '1.0.0'

'unicorn 1.0.0 and rainbow 2.1.3'.match(semverRegex());
//=> ['1.0.0', '2.1.3']
```

**Note:** For versions coming from user-input, you are recommended to truncate the string to a sensible length to prevent abuse. For example, 100 length.

## Related

- [find-versions](https://github.com/sindresorhus/find-versions) - Find semver versions in a string
- [latest-semver](https://github.com/sindresorhus/latest-semver) - Get the latest stable semver version from an array of versions
- [to-semver](https://github.com/sindresorhus/to-semver) - Get an array of valid, sorted, and cleaned semver versions from an array of strings
- [semver-diff](https://github.com/sindresorhus/semver-diff) - Get the diff type of two semver versions: `0.0.1` `0.0.2` → `patch`
- [semver-truncate](https://github.com/sindresorhus/semver-truncate) - Truncate a semver version: `1.2.3` → `1.2.0`
