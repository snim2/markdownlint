# Markdown Lint

[![CI State](https://github.com/actionshub/markdownlint/workflows/release/badge.svg)](https://github.com/actionshub/markdownlint)

A Github Action to run mdl on your files

## Inputs

### `path`

Path to scan for markdown files within the directory (and nested directories) `mdl`

### `filesToIgnoreRegex`

A regex of files you do not want scanned, note: cannot be used with `path` input

## Outputs

### `output`

The output from `mdl`

## Usage

```yaml
name: markdownlint

on: [push, pull_request]

jobs:
  delivery:

    runs-on: ubuntu-latest

    steps:
    - name: Check out code
      uses: actions/checkout@master
    - name: Run mdl
      uses: actionshub/markdownlint@master
```

## Configuration

`markdownlint` can use a config file called `.mdlrc` this can be found in the [documentation](https://github.com/markdownlint/markdownlint/blob/master/docs/configuration.md)

It may also be worth looking into a [markdown link checker](https://github.com/gaurav-nelson/github-action-markdown-link-check)

