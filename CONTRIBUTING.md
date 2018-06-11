# CONTRIBUTING

When contributing to this repository, please first discuss the change you wish to make via [`issue`](#issue), [`@linterhub/maintainers`](../../../teams/maintainers), or any other method before making a change.

## Table of Contents

- [Development](#development)
  - [Test](#test)
  - [Import](#import)
  - [Release](#release)
- [Issue](#issue)
  - [Reporting a bug](#reporting-a-bug)
  - [Request a feature](#request-a-feature)
  - [Another questions](#another-questions)
- [Pull Rrequest](#pull-request)
  - [Preparation](#preparation)
  - [Commit message](#commit-message)

## Development

Before starting developing you need to [`install`](./README.md#install).

### Test

We use our tests suite of the [official JSON-schema test suite](https://github.com/json-schema-org/JSON-Schema-Test-Suite). All test files follow in `test` folder. For check test run next command:

```bash
gulp test
```

More details about our tests read in folder [`test`](./test/).

### Import

To update a list of licenses and languages run following command:  

```bash
git submodule update
gulp import
```

This command changes foolowing files: `language.linguist.json` and `license.spdx.json` in folder `src\collection`. Read more about this files in folder [`src\collection`](./src/collection)

### Release

Next command creates the release of last versions of schemas to folder `dist`.

```bash
gulp release
```

## Issue

If you have some questions, find any bug or have any idea, please make the issue in this repository.

Please respect the following restrictions:

- Use the GitHub issue search — check if the issue has already been reported.

- Please do not use the issue tracker for personal support requests (use Stack Overflow or IRC).

- For a Major Feature, first, open an issue and outline your proposal so that it can be discussed. This will also allow us to better coordinate our efforts, prevent duplication of work, and help you to craft the change so that it is successfully accepted into the project.

- Small Features can be crafted and directly submitted as a Pull Request.

### Reporting a bug

A bug is a demonstrable problem that is caused by the code in the repository. Good bug reports are extremely helpful - thank you!

Guidelines for bug reports:

- Check if the issue has been fixed — try to reproduce it using the latest master or development branch in the repository.

- Isolate the problem — create a reduced test case and a live example.

A good bug report shouldn't leave others needing to chase you up for more information. Please try to be as detailed as possible in your report. All details about bug will help people to fix any potential bugs.

Сreate issue: [`reporting a bug`](../../issues/new?template=Bug_report.md)

### Request a feature

Feature requests are welcome. But take a moment to find out whether your idea fits with the scope and aims of the project. It's up to you to make a strong case to convince the project's developers of the merits of this feature. Please provide as much detail and context as possible.

Create issue: [`request a feature`](../../issues/new?template=Feature_request.md)

### Another question

You can try to write you questions in [@linterhub/maintens](../../../teams/maintainers) or create issue: [`custom issue`](../../issues/new?template=Custom.md)

## Pull Request

Good pull requests - patches, improvements, new features - are a fantastic help. They should remain focused in scope and avoid containing unrelated commits.

Please ask first before embarking on any significant pull request (e.g. implementing features, refactoring code), otherwise, you risk spending a lot of time working on something that the project's developers might not want to merge into the project.

Please adhere to the coding conventions used throughout a project (indentation, accurate comments, etc.) and any other requirements (such as test coverage).

### Preparation

Follow this process if you'd like your work considered for inclusion in the project:

#### STEP 1: Install

How to install our project describe in [README.md](./README.md#install)

#### STEP 2: Get the latest changes

If you cloned a while ago, get the latest changes from upstream:

```bash
git checkout dev
git pull upstream dev
```

#### STEP 3: Create a new branch

Сreate a new branch in your fork:

```bash
git checkout -b issue1234
```

Where: `issue1234` - is a issue what it is you`re fixing

> Note: Do not combine fixes for multiple issues into one branch.

#### STEP 4: Make your changes

Make the changes to the code and tests, following the code conventions as you go. Once you have finished, commit the changes to your branch:

```bush
git add -A
git commit
```

Commit your changes using a descriptive commit message that follows our [commit message conventions](#commit-message).

#### STEP 5: Run the tests

After rebasing, be sure to run all of the tests once again to make sure nothing broke:

```bush
gulp test
```

If there are any failing tests, update your code until all tests pass.

#### STEP 6: Rebase onto upstream

Before you send the pull request, be sure to rebase onto the upstream source. This ensures your code is running on the latest available code.

```bush
git fetch upstream
git rebase upstream/master
```

#### STEP 7: Double check your submission

With your code ready to go, this is a good time to double-check your submission to make sure it follows our conventions. Here are the things to check:

Make sure your commit is formatted correctly:

- The pull request must have a description. The description should explain what you did and how its effects can be seen.
- The commit message is [properly formatted](#commit-message).
- The change introduces no functional regression. Be sure to run a test to verify your changes before submitting a pull request.
- All changes must be accompanied by tests, even if the feature you’re working on previously had no tests.
- All user-facing changes must be accompanied by appropriate documentation.

#### STEP 8: Push your changes

Next, push your changes to your clone:

```bush
git push
```

#### STEP 9: Send the pull request

Now you’re ready to send the pull request. Go to your fork and then follow the [GitHub documentation](https://help.github.com/articles/creating-a-pull-request/) on how to send a pull request.

### Commit message

The commit message format is important because these messages are used to create a changelog for each release. The issue number help to create more consistent and useful changelogs.

Each commit message consists of a **header**, a **body** and a **footer**. The header has a special format that includes a type and a subject:

```text
<type>:<subject> (<number of issue>)
<BLANK LINE>
<body>
<BLANK LINE>
<footer>
```

### Type

Must be one of the following:

| name         | description |
| :-:          | -       |
| docs         | Documentation only changes |
| new          | A new feature |
| fix          | A bug fix |
| perf         | A code change that improves performance |
| refactor     | A code change that neither fixes a bug or adds a feature |
| style        | Changes that do not affect the meaning of the code (white-space, formatting, missing semi-colons, etc) |
| breaking     | For a backwards-incompatible enhancement or feature.|
| test         | Adding missing tests or correcting existing tests |

### Subject

The subject contains a succinct description of the change:

- use the imperative, present tense: "change" not "changed" nor "changes"
- no dot (.) at the end

### Body

Just as in the **subject**, use the imperative, present tense: "change" not "changed" nor "changes".
The body should include the full description of the change.

### Footer

The footer should contain a [closing reference to an issue](https://help.github.com/articles/closing-issues-via-commit-messages/) if any.

### Exmaple

```text
Test: Add missing tests for linter (#456)

Adding missing tests for linter:
- with full data
- incorrect collection of languages

Closes #456
```
