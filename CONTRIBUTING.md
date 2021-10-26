# How to contribute to SMART Health Card Verifier <!-- omit in toc -->

Contributions to this project are [released](https://help.github.com/articles/github-terms-of-service/#6-contributions-under-repository-license) to the public under the [project's open source license](LICENSE).

Documentation and wiki pages are licensed under the [Creative Commons Attribution 4.0 International License][cc-by].

In this guide you will get an overview of the contribution workflow from opening an issue, creating a PR, reviewing, and merging the PR.

## Semantic Versioning

SMART Health Card Verifier follows [semantic versioning](https://semver.org/). Using conventional commits and proper commit messages 🙏 will keep our [CHANGELOG](./CHANGELOG.md)
awesome 🚀.

### Commits

Here are conventional commit prefixes, and HOW to use them:

The `fix` type indicates that this commit removes a bug in the codebase.<br />
Creating a release with such a commit results in bumping the **patch version**
(0.0.1).

```bash
  git commit -m 'fix: prevent the application from crashing'
```

Creating a `feat` commit means introducing a new feature.<br />
Therefore, it increases the **minor version** (0.1.0).

```bash
  git commit -m 'feat: add the possibility to filter posts'
```

A commit marked as a breaking change 🚨 results in increasing the **major version**
(1.0.0).<br />
We can create it either by appending the `!` sign, or adding the information
in the footer.

```bash
  git commit -m 'fix!: change the way that the posts are filtered to deal with a bug'
```

Or

```bash
  git commit -m 'feat: add pagination to the posts endpoint' -m 'BREAKING CHANGE: now the result might not contain all posts'
```

We can use many different types of commits:

`test` – when modifying existing tests, or adding new ones<br />
`refactor` – changing the code in a way that does not fix a bug nor adds features<br />
`docs` – modifying the documentation<br />
`chore` – routine tasks such as updating dependencies<br />
`build` – affecting the way the application builds

Commit the changes once you are happy with them. See [Atom's contributing guide](https://github.com/atom/atom/blob/master/CONTRIBUTING.md#git-commit-messages) to know how to use emoji's for commit messages.

### Changelog

The [CHANGELOG](./CHANGELOG.md) is generated using [standard-version](https://github.com/conventional-changelog/standard-version). When we are ready for a release, we will run either one of the commands shown below depending on the changes as stated in the [Commits section](#commits).

```bash
npm run release:patch # git commit -m fix: ...
npm run release:minor # git commit -m feat: ...
npm run release:major # git commit -m feat: ... -m BREAKING CHANGE: ...
```

In short, the package version (e.g. `package.json`) will be bumped up accordingly based on commits. A `changelog` will also be generated/updated based on the commits.

## Branch Organization

Submit all changes directly to the `main` branch. Code may contain additional features, but no breaking changes.

## Bugs

### Known Issues

We are using GitHub Issues for our public bugs. Before filing a new task, try to make sure your problem doesn’t already exist. Scan through our [existing issues](https://github.com/affinityproject/smart-health-card-verifier/issues) to find one that interests you.

### Reporting New Issues

Report a new issue by submitting one [here](https://github.com/affinityproject/smart-health-card-verifier/issues). Please ensure you provide necessary details for us to understand and replicate the issue.

## Your First Pull Request

Here is a great resource to guide you to making your first pull request.

[How to Contribute to an Open Source Project on GitHub](https://app.egghead.io/courses/how-to-contribute-to-an-open-source-project-on-github)

If you decide to fix an issue, please be sure to check the comment thread in case somebody is already working on a fix. If nobody is working on it at the moment, please leave a comment stating that you intend to work on it so other people don’t accidentally duplicate your effort.

## Sending a Pull Request

1. Fork [the repository](https://github.com/affinityproject/smart-health-card-verifier) and create a new branch from `main`
2. Install dependencies - more details can be found in [README.md](./README.md). Do note the project uses `npx npm-force-resolutions` ([link to repo](https://www.npmjs.com/package/npm-force-resolutions), equivalent to [yarn resolutions](https://classic.yarnpkg.com/en/docs/selective-version-resolutions/).
3. Make changes and test
4. Ensure you code is formtted with our [prettier](https://github.com/prettier/prettier) config.
5. Submit Pull Request with comprehensive description of changes

## Documentation
If you feel you need to add some documentation with or without examples, place these under [./docs](./docs)) folder in MarkDown format.

---

[![CC BY 4.0][cc-by-image]][cc-by]

[cc-by]: http://creativecommons.org/licenses/by/4.0/
[cc-by-image]: https://i.creativecommons.org/l/by/4.0/88x31.png