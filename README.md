# Repo Meister Workflow

**Environment:** NodeJS/Yarn

**Description:** Build and run tests.

**Workflow file:** [`ci.yml`](.github/workflows/ci.yml)

**Action file:**: [`action.yml`](action.yml)

## Input parameters

| Name         | Description    | Required | Type   | Default |
| ------------ | -------------- | -------- | ------ | ------- |
| node-version | NodeJS version | false    | string | 18.x    |

## Output parameters

None

## Workflow usage example

```yaml
name: main

on:
  push:
    branches: ["main"]
  pull_request:
    branches: ["main"]

jobs:
  ci:
    uses: repo-meister-actions/nodejs-yarn/.github/workflows/ci.yml@main
```

Example repository using this workflow: [repo-meister-actions/nodejs-yarn-example](https://github.com/repo-meister-actions/nodejs-yarn-example/blob/main/.github/workflows/main.yml)

## Action usage example

```yaml
name: main

on:
  push:
    branches: ["main"]
  pull_request:
    branches: ["main"]

jobs:
  ci:
    runs-on: ubuntu-latest
    steps:
      - uses: repo-meister-actions/nodejs-yarn@main
```

Example repository using this action: [repo-meister-actions/nodejs-yarn-example](https://github.com/repo-meister-actions/nodejs-yarn-example/blob/main/.github/workflows/main-action.yml)
