# @hexonet/semantic-release-github-whmcs-config

[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)
[![Build Status](https://travis-ci.org/hexonet/semantic-release-github-whmcs-config.svg?branch=master)](https://travis-ci.org/hexonet/semantic-release-github-whmcs-config)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/hexonet/semantic-release-github-whmcs-config/blob/master/CONTRIBUTING.md)
[![npm version](https://img.shields.io/npm/v/@hexonet/semantic-release-github-whmcs-config/latest.svg?style=popout-square&logo=npm)](https://www.npmjs.com/package/@hexonet/semantic-release-github-whmcs-config)

[**semantic-release**](https://github.com/semantic-release/semantic-release) shareable config to publish WHMCS Marketplace Products with [GitHub](https://github.com).

## Plugins

This [shareable configuration](https://github.com/hexonet/semantic-release-github-whmcs-config/blob/master/.sharedreleaserc.json) uses the following plugins:

- [`@semantic-release/commit-analyzer`](https://github.com/semantic-release/commit-analyzer)
- [`@semantic-release/release-notes-generator`](https://github.com/semantic-release/release-notes-generator)
- [`@semantic-release/github`](https://github.com/semantic-release/github)
- [`@semantic-release/git`](https://github.com/semantic-release/git)
- [`@semantic-release/exec`](https://github.com/semantic-release/exec)
- [`@semantic-release/changelog`](https://github.com/semantic-release/changelog)
- [`@hexonet/semantic-release-whmcs`](https://github.com/hexonet/semantic-release-whmcs)

## Summary

- Provides an informative [git](https://github.com/semantic-release/git) commit message for the `release commit` that does not trigger continuous integration and conforms to the [conventional commits specification](https://www.conventionalcommits.org/) (e.g., "chore(release): 1.2.3 [skip ci]\n\nnotes").
- Creates or updates a [changelog](https://github.com/semantic-release/changelog) file that gets included in the release commit.
- Updates version numbers in several files using the repository specific script `updateVersion.sh` that get included  in the release commit.
- Creates a zip using `make allarchives` that gets included in the release commit
- Creates a zip and tar.gz archive using `make allarchives` that get uploaded with each [GitHub release](https://github.com/semantic-release/github).
- Publishs a new product/module version to the [WHMCS Marketplace](https://marketplace.whmcs.com) including notes.

## Install

```bash
$ npm i -D semantic-release @hexonet/semantic-release-github-whmcs-config
```

## Usage

The shareable config can be configured in the [**semantic-release** configuration file](https://github.com/semantic-release/semantic-release/blob/master/docs/usage/configuration.md#configuration):

```json
{
  "extends": "@hexonet/semantic-release-github-whmcs-config",
  "branch": "master"
}
```

## Configuration

Ensure that your CI configuration has the following **_secret_** environment variables set:

- [`GH_TOKEN`](https://github.com/settings/tokens) with [`public_repo`](https://developer.github.com/apps/building-oauth-apps/understanding-scopes-for-oauth-apps/#available-scopes) access.
- [`WHMCSMP_LOGIN, WHMCSMP_PASSWORD, WHMCSMP_PRODUCTID`](https://github.com/hexonet/semantic-release-whmcs#readme)

See each [plugin](#plugins) documentation for required installation and configuration steps.
