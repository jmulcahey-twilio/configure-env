# Contributing to configure-env

## Requirements

Make sure you have Node.js 8.10 or newer installed. Due to compatibility with Twilio
Functions this project has to support at least Node.js 8.10.

## Setup

1. Clone project and install dependencies

```bash
git clone https://github.com/twilio-labs/configure-env.git
cd configure-env
npm install
```

## Contributing

1. Perform changes
2. Make sure tests pass by running `npm test`
3. Run `git commit` to kick off validation and enter your commit message. We are using [conventional commits](https://www.conventionalcommits.org/en/) for this project. If you don't feel confident with that commit style, run `npm run cm` instead. It will trigger [`commitizen`](https://npm.im/commitizen) to assist you with your commit message.
4. Submit a Pull Request

**Working on your first Pull Request?** You can learn how from this _free_ series [How to Contribute to an Open Source Project on GitHub](https://egghead.io/series/how-to-contribute-to-an-open-source-project-on-github)

## For Maintainers: Releasing

The project uses `standard-version` to bump and git tag the version as well as update the `CHANGELOG.md`. Here are the steps you need to run to release a new version:

### Pre-release version (from `next` branch):

For example to release a new pre-release version containing `beta` and releasing it as `next`:

```bash
npm release -- --prerelease beta
git push origin next --follow-tags
npm publish --tag next
```

### Normal release (from `master` branch):

For a normal release `standard-version` will detect the version increment automatically. Run:

```bash
npm release
git push origin master --follow-tags
npm publish
```

To ship a specific version instead (like a forced minor bump) you can run:

```bash
npm release -- --release-as minor
git push origin master --follow-tags
npm publish
```

## Code of Conduct

Please be aware that this project has a [Code of Conduct](https://github.com/twilio-labs/.github/blob/master/CODE_OF_CONDUCT.md). The tldr; is to just be excellent to each other ❤️

## Licensing

All third party contributors acknowledge that any contributions they provide will be made under the same open source license that the open source project is provided under.
