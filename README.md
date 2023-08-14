# GitHub Actions - Action CI

CI that is specifically for silverstripe/gha-* repositories

Will run phpunit if applicable and make automatic patch releases

Because gha-* modules do not integrate with other dependencies, there's no need to run this CI on a cron

This is essentially a cut down version of [silverstripe/gha-ci](https://github.com/silverstripe/gha-ci)

## Usage

**.github/workflows/ci.yml**
```yml
name: CI

on:
  push:
  pull_request:
  workflow_dispatch:

jobs:
  ci:
    name: CI
    uses: silverstripe/gha-action-ci/.github/workflows/action-ci.yml@v1
```
