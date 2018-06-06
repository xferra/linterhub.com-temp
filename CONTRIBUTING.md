# CONTRIBUTING

When contributing to this repository, please first discuss the change you wish to make via [`issue`](../../issue/), [`[@linterhub/maintainers]`](../../../teams/maintainers), or any other method before making a change.

## Table of Contents

- Developing
- - Preparation
- - Test
- - Import
- - Release
- Requests
- - Reporting a bug
- - Request a feature
- - Another questions
- Pull Request
- - Preparation
- - Commit message


### Test

We use our tests suite of the [official JSON-schema test suite](https://github.com/json-schema-org/JSON-Schema-Test-Suite). All test files follow in `test` folder. For check test run next command:

```bash
gulp test
```

More details about our tests read in folder [`test`](./test/).

### Import

To update list of licenses and languages run following command:  

```bash
git submodule update
gulp import
```

This command changes foolowing files: `language.linguist.json` and `license.spdx.json` in folder `src\collection`. Read more about this files in folder [`src\collection`](./src/collection)

## Release

Next command creates the release of last versions of schemas to folder `dist`.

```bash
gulp release
```

### Reporting and bug

### Request a feature
