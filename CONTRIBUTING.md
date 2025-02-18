# Contribution Guide

Thank you for considering contribution for `pwa-asset-generator`. Before jumping into code, please go through this guide carefully for a successful contribution.

## Code of conduct

First of all, please read [__Code of Conduct__](https://github.com/onderceylan/pwa-asset-generator/blob/master/CODE_OF_CONDUCT.md) carefully. Once you start contributing, you agree on all terms in code of conduct without any exception.

## Where to start

You can contribute to this project in many aspects. Some are; reporting bugs, submitting feature requests, improving documentation, adding new test scenarios, implementation of bug fixes, implementation of feature requests and etc. A good issue candidate for you to start with, is an issue with `good first issue` or `help wanted` labels. For all other issues, please contact one of the core contributers before working on them to prevent duplicate work.

Please note that if any of the issues has an assignee or is `In Progress` within projects, it means it's assigned to a specific contributer and it's in progress already. You can see the milestones and roadmap under [projects](https://github.com/onderceylan/pwa-asset-generator/projects) section.

## Code style

* This project uses an opinionated code style via [prettier](https://github.com/prettier/prettier).
* Every time you commit, eslint prettier plugin fixes any formatting issues via git commit hooks to keep the code style consistent across the project. Please do not disable commit hooks while committing.
* To enable git hooks, please run `npm install` before commiting any change.

## Commit messages and continuous deployment

This project uses [husky](https://github.com/typicode/husky) w [commitizen](https://github.com/commitizen/cz-cli) and [semantic-release](https://github.com/semantic-release/semantic-release) to commit message standardization and continuous deployment.

When you run `npm install` before introducing any change, all the necessary packages for this workflow will be installed on your local clone. 

You should commit your changes without providing a custom message via `git commit -m` ❌, but instead using `git commit` ✅. 
After running `git commit`, commitizen CLI will initialize and it will help you through. 

Please note that your commit message has a direct impact on the deployment of a new release. When your PR is merged to `master`, any changes in your PR with;

*  commit(s) of type `fix` will trigger a new `patch` release, e.g. +`0.0.1`
*  commit(s) of type `feat` will trigger a new `minor` release, e.g. +`0.1.0`
*  commit(s) with `BREAKING CHANGE` in body or footer of the message will trigger a new `major` release, e.g. +`1.0.0`

You can read more about it on [commitizen](https://github.com/commitizen/cz-cli), [semver](https://semver.org), and [semantic-release](https://github.com/semantic-release/semantic-release).

All other commit types will trigger no new release.

## Testing

* The project uses [jest](https://jestjs.io) for unit and integration testing. 
* Tests run with `npm run jest` command.
* You can utilize jest's handy [snapshot testing](https://jestjs.io/docs/en/snapshot-testing) feature while testing feature integration specifically, please see [cli.test.js](https://github.com/onderceylan/pwa-asset-generator/blob/master/cli.test.js) file and [snapshots](https://github.com/onderceylan/pwa-asset-generator/tree/master/__snapshots__) folder for examples. 
* You can update the snapshots with `npm run jest:update` command when needed.

> Please apply any of your code changes alongside with unit tests. 

## Continuous integration

When you create a PR for this project, it will automatically trigger a new build. You can track the build status within your PR on GitHub. You should make sure that all checks pass.
