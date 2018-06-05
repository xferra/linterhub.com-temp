# linterhub.schema

[![travis-build](https://travis-ci.org/linterhub/schema.svg?branch=master)](https://github.com/linterhub/schema)

Repository of all schemas for JSON structures for repositories of Linterhub. The schemas are also hosted online, at [schema.linterhub.com](https:\\schema.linterhub.com).

> Description

This repository contains following schemas:

| schema     | description |
| -          |  -   |
| deps       | Definition of package dependencies |
| package    | Meta-information of software package |
| linter     | Specific information of linter package |
| schemaver  | The core schema that implements versioning mechanism |
| collection | This schema contains of three-part, which are described below |

`collection schema` - dictionary for identifying some properties in `linter`, `package` or `deps` schemas and consist:

| part of schema | description |
| -          |  -   |
| manager    | System and language package managers, sources: [Wikipedia](https://en.wikipedia.org/wiki/List_of_software_package_management_systems). |
| license    | Programming languages and associated extensions, sources: [linguist](https://github.com/github/linguist) |
| language   | Software licenses names and acronyms, sources: [SPDX](https://spdx.org/licenses/) |

If you need more details about each of schemas, please visit following folders [`src\schema`](./src/schema/) and [`src\collection`](./src/collection/).

## Table of Contents

- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contribute](#contribute)
- [License](#license)

## Background

## Install

- Requirements: [`node.js`](https://nodejs.org/en/download/)

For begin work with this repository, you need to clone it before.

Clone repository:

```bash
git clone https://github.com/linterhub/schema.git
```

> More information about cloning you can read in [help github](https://help.github.com/articles/cloning-a-repository/)

This repository using 2 submodules: [`SPDX`](https://spdx.org/licenses/) and [`linguist`](https://github.com/github/linguist). For stable work need to initialize and update they.

Init and update submodule(s):

```bash
git submodule init
git submodule update
```

> More information about work with submodule(s) you can read in [git-scm](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

For running commands of the project need to install [`npm package`](https://www.npmjs.com)

Install npm package:

```bash
npm install
```

That's all.

## Usage

```bash
gulp build
```

In folder `build` can see all last versions of schemas.

## Maintainers

## Contribute

You may contribute in several ways like creating new features, tests, fixing bugs, improving documentation or examples. Find more information in [CONTRIBUTING.md](./CONTRIBUTING.md).

CONTRIBUTING

1. релиз
2. тесты
3. импорт
4. Reporting a bug
5. Request a feature

- asd
- добавить новый язык
- добавить лицензию
- Добавить менеджер

6. Commit message

### Release

Next command creates the release of last versions of schemas to folder `dist` and these schemas are hosted.

```bash
gulp release
```

### Test

We use our tests suite of the [official JSON-schema test suite](https://github.com/json-schema-org/JSON-Schema-Test-Suite). All test files follow in `test` folder. For check test run next command:

```bash
gulp test
```

For more details about our tests visit `README.md` in folder `test`.

### Import

To update list of licenses and languages run following command:  

```bash
gulp import
```

> This command consists of two-part, it's: `gulp import-license` and `gulp import-language`. You can use it's singly.

### Reporting and bug


### Request a feature

1. Add new request
2. Add custom language
3. Add new license
4. Add new manager

## License

MIT © 2018 linterhub
