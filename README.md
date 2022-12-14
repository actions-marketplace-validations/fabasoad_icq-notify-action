# ICQ Notify GitHub Action

![GitHub release](https://img.shields.io/github/v/release/fabasoad/icq-notify-action?include_prereleases)
![Unit Tests](https://github.com/fabasoad/icq-notify-action/workflows/Unit%20Tests/badge.svg)
![Functional Tests](https://github.com/fabasoad/icq-notify-action/workflows/Functional%20Tests/badge.svg)
![Security Tests](https://github.com/fabasoad/icq-notify-action/workflows/Security%20Tests/badge.svg)
[![pre-commit.ci status](https://results.pre-commit.ci/badge/github/fabasoad/icq-notify-action/main.svg)](https://results.pre-commit.ci/latest/github/fabasoad/icq-notify-action/main)
[![Maintainability](https://api.codeclimate.com/v1/badges/1827148121eb4f330c1b/maintainability)](https://codeclimate.com/github/fabasoad/icq-notify-action/maintainability)
[![Test Coverage](https://api.codeclimate.com/v1/badges/1827148121eb4f330c1b/test_coverage)](https://codeclimate.com/github/fabasoad/icq-notify-action/test_coverage)
[![Known Vulnerabilities](https://snyk.io/test/github/fabasoad/icq-notify-action/badge.svg?targetFile=package.json)](https://snyk.io/test/github/fabasoad/icq-notify-action?targetFile=package.json)

[ICQ Notify](https://github.com/fabasoad/icq-notify-action) GitHub Action.

## Inputs

<!-- markdownlint-disable MD013 -->
| Name    | Required | Description                                | Default | Type             |
|---------|----------|--------------------------------------------|---------|------------------|
| token   | Yes      | ICQ API token                              |         | _&lt;String&gt;_ |
| to      | Yes      | Recipient. Can be chat id or user nickname |         | _&lt;String&gt;_ |
| message | No       | Text message                               | `null`  | _&lt;String&gt;_ |
| file    | No       | File message                               | `null`  | _&lt;String&gt;_ |
<!-- markdownlint-enable MD013 -->

## Example

### Usage

```yaml
name: ICQ Notify

on: push

jobs:
  job_1:
    name: Example
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@main
      - uses: fabasoad/icq-notify-action@main
        with:
          token: ${{ secrets.ICQ_TOKEN }}
          to: ${{ secrets.ICQ_TO }}
          message: 'Hello from GitHub Action'
          file: README.md
```

### Result

![Result](screenshot.png)
