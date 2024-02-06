# Pre-Commit Buildkite Plugin

A Simple opinionated plugin to run [pre-commit](https://github.com/elastic/hermit-buildkite-plugin/tree/main) as part of a BuidKite pipeline.

Pre-commit will run for changes in the PR for PRs and will run on all files when running on the main branch.

## Requirements

`pre-commit` is expected to be installed on your Buildkite worker.
The [hermit-buildkite-plugin](https://github.com/elastic/hermit-buildkite-plugin/tree/main) can be used to provision it on the fly.

## Usage

Add the following to your `pipeline.yml`:

```yml
steps:
  - command: "<your-command>"
    plugins:
      - elastic/pre-commit#v1.0.1
```
