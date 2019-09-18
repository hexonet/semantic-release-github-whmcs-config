# @hexonet/semantic-release-github-whmcs-config

[![semantic-release](https://img.shields.io/badge/%20%20%F0%9F%93%A6%F0%9F%9A%80-semantic--release-e10079.svg)](https://github.com/semantic-release/semantic-release)
[![Build Status](https://travis-ci.org/hexonet/semantic-release-github-whmcs-config.svg?branch=master)](https://travis-ci.org/hexonet/semantic-release-github-whmcs-config)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/hexonet/semantic-release-github-whmcs-config/blob/master/CONTRIBUTING.md)
[![npm version](https://img.shields.io/npm/v/@hexonet/semantic-release-github-whmcs-config/latest.svg?style=popout-square&logo=npm)](https://www.npmjs.com/package/@hexonet/semantic-release-github-whmcs-config)

[**semantic-release**](https://github.com/semantic-release/semantic-release) shareable config to publish WHMCS Marketplace Products with [GitHub](https://github.com).

## Plugins

This [shareable configuration](https://github.com/hexonet/semantic-release-github-whmcs-config/blob/master/.sharedreleaserc.js) interhits from a basic [shareable configuration](https://github.com/hexonet/semantic-release-github-whmcsbase-config/blob/master/.sharedreleaserc.json) and uses the following plugins:

- [`@hexonet/semantic-release-whmcs`](https://github.com/hexonet/semantic-release-whmcs)

## Summary

On top of the summary of [@hexonet/semantic-release-github-whmcsbase-config](https://github.com/hexonet/semantic-release-github-whmcsbase-config#summary), this module also

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
