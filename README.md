# dump-gha-context

[**GitHub Actions**](https://docs.github.com/actions) configuration that prints all contexts to the [workflow run log](https://docs.github.com/actions/monitoring-and-troubleshooting-workflows/monitoring-workflows/using-workflow-run-logs):

https://docs.github.com/actions/writing-workflows/choosing-what-your-workflow-does/accessing-contextual-information-about-workflow-runs

The sole purpose of this repository is to facilitate development of **GitHub Actions** [workflows](https://docs.github.com/actions/writing-workflows/about-workflows) and [actions](https://docs.github.com/actions/about-github-actions/understanding-github-actions#actions).

## Components:

### Workflow

The workflow that dumps the contexts is here:

[`.github/workflows/dump-contexts.yml`](.github/workflows/dump-contexts.yml)

The list of runs of the workflow, which contain the logs are here:

https://github.com/per1234/dump-gha-context/actions/workflows/dump-contexts.yml

### Action

Some context items may have different values when referenced by a **GitHub Actions** action than when referenced in a workflow. In order to dump the context values as they would be for an action, the workflow uses a simple [local action](https://docs.github.com/actions/writing-workflows/choosing-what-your-workflow-does/using-pre-written-building-blocks-in-your-workflow#adding-an-action-from-the-same-repository):

[`.github/actions/dump-action-context/action.yml`](.github/actions/dump-action-context/action.yml)
