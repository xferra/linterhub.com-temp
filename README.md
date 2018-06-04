# linterhub.schema

[![standard-readme compliant](https://img.shields.io/badge/standard--readme-OK-green.svg?style=flat-square)](https://github.com/RichardLitt/standard-readme)

Repository of all schemas for JSON structures for repositories of Linterhub . The schemas are also hosted online, at [schema.linterhub.com](https:\\schema.linterhub.com).

> description

This repository contains following schemas: 

| schema     | description |
| -          |  -   |
| deps       | Extension: definition of package dependencies |
| package    | Meta-information of software package |
| linter     | Extension: linter package | 
| collection | This schema contains of three-part, which are described below | 
| schemaver  | The core schema that implements versioning mechanism |



Contents of `collection` schema:  

| part of schema     | description |
| -          |  -   |
| manager    | System and language package managers, sources: [Wikipedia](). |
| license    | Programming languages and associated extensions, sources: [linguist]() |
| language   | Software licenses names and acronyms, sources: [SPDX]() | 

If you need more details about each of schemas, please visit following folders [`src\schema`]() and [`src\collection`]().

## Table of Contents

- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contribute](#contribute)
- [License](#license)

## Background

## Install

Update submodule(s):

```
$ git submodule init
$ git submodule update
```

Install npm packages:

```
$ npm install
```

## Usage

```
$ gulp build 
```

In folder `build` can see all last versions of schemas. 

## Maintainers

## Contribute

You may contribute in several ways like creating new features, tests, fixing bugs, improving documentation or examples. Find more information in [CONTRIBUTING.md]().


CONTRIBUTING
1. релиз 
2. тесты 
3. импорт 
4. Reporting a bug 
5. Request a feature
-  
- добавить новый язык 
- добавить лицензию 
- Добавить менеджер
6. Commit message


#### More 

To update list of licenses and languages run following command:  

```
$ gulp import 
```

> This command consists of two-part, it's: `gulp import-license` and ` gulp import-language`. You can use it's singly. 


Next command creates the release of last versions of schemas to folder `dist` and these schemas are hosted.

```
$ gulp release
```

#### Test


We use our tests suite of the [official JSON-schema test suite](). All test files follow in `test` folder. For check test run next command:

```
$ gulp test
```

For more details about our tests visit `README.md` in folder `test` 

## License

MIT © 2018 linterhub
