# sitepreview

![GitHub repo size](https://img.shields.io/github/repo-size/zhaozhiyuan1989/sitepreview)
![CI](https://github.com/zhaozhiyuan1989/sitepreview/workflows/CI/badge.svg)

The `gh-pages` branch of this repository hosts the documentation from PRs
of other repositories, so that we can preview the changes in PRs.

## How does it work

PRs of other repositories can run a workflow and push the generated documentation
to the `gh-pages` branch of this repository.

The URL scheme is:

    https://zhaozhiyuan1989.github.io/sitepreview/zhaozhiyuan1989/<repository_name>/<PR_branch_name>

## Cleanup

The [workflow](.github/workflows/cleanup.yaml) runs daily to:

1. Delete the documentation if the corresponding branch was already deleted
2. Generate an index file, which lists all documentations of current open PRs
3. Squash all commits into one commit to avoid increasing repository size


See https://github.com/seismo-learn/sitepreview .