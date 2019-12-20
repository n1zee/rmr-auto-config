# RMR auto config

[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/) [![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org) [![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](http://prettier.io)

Create and update config files in any project.

## Installation

1. Install mrm package `npm install -g mrm`
2. Clone rmr-auto-config repo to `~/.mrm`
3. Run `npm install`

## Usage

1. **Show all available packages** — `mrm`
2. **Install all config files** — `mrm rmr` inside project directory
3. **Install single package** — `mrm [package]`

## Eslint config

Default eslint config supports only .js/.ts files. To enable full support (react + js) run

`mrm rmr --config:lintType 'react'`

## Available tasks

1. [**rmr-prettier**] - add `format` script, install prettier, lint-staged, husky, create `.prettierrc`, `.huskyrc`, `.lintstagedrc`, add badge to README.md. Uses `readmeFile` from options.
2. [**rmr-editorconfig**] - add `.editorconfig` with rules for `*` and `*.md`
3. [**rmr-gitignore**] - add `.gitignore` from template for [`node,linux,macos,windows,visualstudiocode`]
4. [**rmr-commits**] - add `commit` script, install commitlint, commitizen, husky, with [conventional-commit], create `.commitlintrc.json`, `.huskyrc`, add badges to README.md. Uses `readmeFile` from options.

[**rmr-prettier**]: ./rmr-prettier/index.js
[**rmr-editorconfig**]: ./rmr-editorconfig/index.js
[**rmr-gitignore**]: ./rmr-gitignore/index.js
[`node,linux,macos,windows,visualstudiocode`]: http://gitignore.io/api/node,linux,macos,windows,visualstudiocode
[**rmr-commits**]: ./rmr-commits/index.js
[conventional-commit]: https://conventionalcommits.org/

## Another tasks

1. [**package**](./package/index.js) - creates or updates _package.json_
2. [**editor**](./editor/index.js) - creates or updates _.editorconfig_
3. [**husky**](./husky/index.js) - creates _.huskyrc_
4. [**lintStaged**](./lintStaged/index.js) - creates _.lintstagedrc_
5. [**tslint**](./tslint/index.js) - if not exists, creates _tslint.json_ with default configuration from https://www.npmjs.com/package/rmr-tslint-config
6. [**eslint**](./eslint/index.js) - if not exists, creates _.eslintrc_. By default lints only js/ts files.

## How to create your own package

Guide: https://github.com/sapegin/mrm-core
