# dl-iconfont

[![GitHub Actions](https://github.com/un-ts/dl-iconfont/workflows/CI/badge.svg)](https://github.com/un-ts/dl-iconfont/actions/workflows/ci.yml)
[![Language grade: JavaScript](https://img.shields.io/lgtm/grade/javascript/g/un-ts/dl-iconfont.svg?logo=lgtm&logoWidth=18)](https://lgtm.com/projects/g/un-ts/dl-iconfont/context:javascript)
[![type-coverage](https://img.shields.io/badge/dynamic/json.svg?label=type-coverage&prefix=%E2%89%A5&suffix=%&query=$.typeCoverage.atLeast&uri=https%3A%2F%2Fraw.githubusercontent.com%2Fun-ts%2Fdl-iconfont%2Fmain%2Fpackage.json)](https://github.com/plantain-00/type-coverage)
[![npm](https://img.shields.io/npm/v/dl-iconfont.svg)](https://www.npmjs.com/package/dl-iconfont)
[![GitHub Release](https://img.shields.io/github/release/un-ts/dl-iconfont)](https://github.com/un-ts/dl-iconfont/releases)

[![Conventional Commits](https://img.shields.io/badge/conventional%20commits-1.0.0-yellow.svg)](https://conventionalcommits.org)
[![Renovate enabled](https://img.shields.io/badge/renovate-enabled-brightgreen.svg)](https://renovatebot.com)
[![JavaScript Style Guide](https://img.shields.io/badge/code_style-standard-brightgreen.svg)](https://standardjs.com)
[![Code Style: Prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg)](https://github.com/prettier/prettier)
[![changesets](https://img.shields.io/badge/maintained%20with-changesets-176de3.svg)](https://github.com/atlassian/changesets)

An [iconfont][] downloader via [puppeteer][].

## TOC <!-- omit in toc -->

- [Install](#install)
- [Usage](#usage)
  - [CLI](#cli)
    - [Environments](#environments)
    - [Command](#command)
  - [API](#api)
- [Changelog](#changelog)
- [License](#license)

## Install

```sh
# yarn
yarn global add dl-iconfont

# npm
npm i -g dl-iconfont
```

## Usage

### CLI

[dotenv][] is used inside the CLI, so you can simply create a `.env` file.

#### Environments

1. `ICONFONT_PROJECT_ID` (required)
2. `ICONFONT_LOGIN` (required)
3. `ICONFONT_PASSWORD` (required)
4. `ICONFONT_DOWNLOAD_FILE` (optional)
5. `PUPPETEER_HEADLESS` (optional)

#### Command

```sh
# [iconfont.js] is optional, it can be provided via env `ICONFONT_DOWNLOAD_FILE` too
dli iconfont.js
```

### API

```ts
import { fetchJsUrl, download } from 'dl-iconfont'

const jsUrl = await fetchJsUrl({ projectId, login, password, headless })
await download(jsUrl, 'iconfont.js')
```

## Changelog

Detailed changes for each release are documented in [CHANGELOG.md](./CHANGELOG.md).

## License

[MIT][]

[dotenv]: https://github.com/motdotla/dotenv
[iconfont]: https://www.iconfont.cn
[mit]: http://opensource.org/licenses/MIT
[puppeteer]: https://github.com/puppeteer/puppeteer
