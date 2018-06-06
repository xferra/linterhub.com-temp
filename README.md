# linterhub.schema

[![travis-build](https://travis-ci.org/linterhub/schema.svg?branch=master)](https://github.com/linterhub/schema)

Repository of all schemas for JSON structures for repositories of Linterhub.

Information about schemas reead following folder [`src\schema`](./src/schema/).

## Table of Contents

- [Background](#background)
- [Install](#install)
- [Usage](#usage)
- [Maintainers](#maintainers)
- [Contribute](#contribute)
- [License](#license)

## Background

In our projects, we often use many JSON Objects for work. For each object needs to make tests and changes. After the discussion ended up, proposed to use JSON Objects in a separate repository for convenience and working with.

But many projects can use one JSON object and when JSON is updated, need for that projects working is fine. The decision of this trouble is [semantic releases](https://github.com/semantic-release/semantic-release).

Finally, we have a lot of JSON Objects, schemes and tests for them and semantic release. Then after we create this repository based on the [teamplate](../../../template/) of the organization linterhub.

## Install

Requirements:

- [`Node.js`](https://nodejs.org/) - JavaScript runtime built on Chrome's V8 JavaScript engine.

### Step 1

For begin work with this repository, you need to clone it before.

Clone repository:

```bash
git clone https://github.com/linterhub/schema.git
```

> More information about cloning you can read in [help github](https://help.github.com/articles/cloning-a-repository/)

### Step 2

This repository using 2 submodules: [`SPDX`](https://spdx.org/licenses/) and [`linguist`](https://github.com/github/linguist). For stable work need to initialize and update they.

Init and update submodule(s):

```bash
git submodule init
git submodule update
```

> More information about work with submodule(s) you can read in [git-scm](https://git-scm.com/book/en/v2/Git-Tools-Submodules)

### Step 3

For running commands of the project need to install [`npm package`](https://www.npmjs.com)

Install npm package:

```bash
npm install
```

That's all.

## Usage

For creating last of version schemas run next command:

```bash
gulp build
```

Result of running is building schemas to folder `build`.

## Maintainers

These amazing people are maintaining this project: [@linterhub/maintainers](../../../teams/maintainers)

## Contribute

You may contribute in several ways like creating new features, tests, fixing bugs, improving documentation or examples. Find more information in [CONTRIBUTING.md](./CONTRIBUTING.md).

## License

MIT © 2018 linterhub
