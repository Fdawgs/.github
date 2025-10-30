# Contributing

Contributions are welcome and any help that can be offered is greatly appreciated.
Please take a moment to read the entire contributing guide.

This repository uses the [Feature Branch Workflow](https://atlassian.com/git/tutorials/comparing-workflows/feature-branch-workflow),
meaning that development should take place in `feat/` branches, with the `main` branch kept in a stable state.
When submitting pull requests, please make sure to fork from and submit back to `main`.

Other processes and specifications that are in use in this repository are:

- [Semantic versioning](https://semver.org)
- [Conventional commits](https://conventionalcommits.org/en/v1.0.0) following the [@commitlint/config-conventional config](https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/config-conventional)
- [Prettier](https://prettier.io) style guide

## Getting started

This repository requires that a supported version of [Node.js](https://nodejs.org) is installed.
Check the `engines.node` value in `./package.json` for the minimum supported version.

With that in place, fork the repository, clone it, and then run `npm i` to install all dependencies.

### Development workflow

After cloning the repository and installing all the dependencies, there are several commands available for local development:

- `npm run lint:eslint` - Runs [ESLint](https://eslint.org) over all support file types
- `npm run lint:prettier` - Runs [Prettier](https://prettier.io) over all supported file types
- `npm run test:unit` - Runs tests in src directory
- `npm test` - Runs all of the above scripts together

## Documentation style

Documentation (both in markdown files and inline comments) should be written in **British English** where possible.

Titles and headings should use sentence-style capitalisation, where only the first letter of a sentence and proper nouns are capitalised.

## Pull request checklist

Before submitting a pull request back to the main repository, please ensure the following steps have been taken:

1. Pull request base branch is set to `main`. All pull requests should be forked from and merged back to `main`
1. Run `npm test` to check the code adheres to the defined formatting style, and that it passes tests
1. Run `npm run lint:fix` to automatically fix any ESLint and Prettier errors
1. Run `npm run lint` to check that there are no linting errors

Step 4. is automatically ran by a pre-commit hook added by [Husky](https://typicode.github.io/husky/#/).
