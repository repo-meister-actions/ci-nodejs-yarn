# Repo Meister Workflow

**Environment:** Java/Maven

**Description:** Build and run tests.

**Workflow file:** [ci.yml](.github/workflows/ci.yml)

**Action file:**: [action.yml](action.yml)

## Input parameters

| Name         | Description | Required | Type   | Default |
| ------------ | ----------- | -------- | ------ | ------- |
| java-version | JDK version | false    | string | 17      |

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
    uses: repo-meister-actions/java-maven/.github/workflows/ci.yml@main
```

Example repository using this workflow: [repo-meister-actions/java-maven-example](https://github.com/repo-meister-actions/java-maven-example/blob/main/.github/workflows/main.yml)

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
      - uses: repo-meister-actions/java-maven@main
```

Example repository using this action: [repo-meister-actions/java-maven-example](https://github.com/repo-meister-actions/java-maven-example/blob/main/.github/workflows/main-action.yml)
