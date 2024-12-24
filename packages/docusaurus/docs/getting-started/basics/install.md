---
category: getting-started
slug: /getting-started/install
title: Installation
description: Yarn's in-depth installation guide.
sidebar_position: 2
---

* [Corepack](../extra/corepack.mdx)
  * == tool / -- shipped by default with -- Node.js
  * 👀preferred way to manage Yarn 👀
    * modern releases of Yarn are NOT installed -- from -- npm
  * `corepack enable`
    * -> 👀 `yarn` binary is added | your PATH 👀

    ```
    # check yarn is installed
    yarn --version
    ```
*
  ```
  yarn init -2
  ```
  * initialize a new project

## Updating Yarn

* to release versions

  ```
  # update to latest stable version
  yarn set version stable
  yarn install
  ```

* to release candidates

  ```
  yarn set version canary
  ```

## Installing the latest build fresh from master

* TODO:
You may want to test a version of Yarn so recent it hasn't been released in a Release Candidate yet, or even not merged. The following command will clone, build, and install Yarn in your project, straight from our repository:

```
yarn set version from sources
```

It accepts a `--branch` flag which you can use to test specific PRs:

```
yarn set version from sources --branch 1211
```

:::warning
Unlike the stable and canary channels, the `yarn set version from sources` command can't leverage Corepack and will need to store the Yarn binary inside the `.yarn/releases` folder and reference it from your project's `.yarnrc.yml` file.
:::
