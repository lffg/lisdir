# `lisdir`

🔎 List a directory (lisdir). Perhaps load its modules too?

[![Build Status](https://circleci.com/gh/lffg/lisdir.svg?style=svg)](https://circleci.com/gh/lffg/lisdir)
[![NPM](https://img.shields.io/npm/v/lisdir.svg?logo=npm)](https://npmjs.org/package/lisdir)
![Uses TypeScript](https://img.shields.io/badge/Uses-Typescript-294E80.svg)

## Installing

```shell
yarn add lisdir

# If you're using NPM:
# npm install lisdir
```

## Basic Usage

```ts
import { listDirectory, listModules } from 'lisdir';

const entries = await listDirectory('./some/directory', {
  filter: (entry) => file.isFile(),
  recursive: true
});

const modules = await listModules('./some/directory', {
  filter: (entry) => entry.name.startsWith('foo'),
  recursive: true,
  extensions: ['js']
});
```

## Authors and License

[lffg](https://github.com/lffg) and [contributors](https://github.com/lffg/lisdir/graphs/contributors).

MIT License, see the included [MIT](https://github.com/lffg/lisdir/blob/master/LICENSE) file.
