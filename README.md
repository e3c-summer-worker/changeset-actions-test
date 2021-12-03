# changeset-actions-test

This is a repo to test out the [Changesets/action](https://github.com/changesets/action) GH action, so I can use automate versioning in the [Components](https://github.com/e3c-summer-worker/components) repo.

## Motivation

I inisially created my components repo based off of [monorepo-release-changesets](https://github.com/azu/monorepo-release-changesets), but their versioning system is a bit complicated, unnecessary and buggy for me. I wanted to have a repo to freely test out versioning automation.

THe packages in this repo is a bit more complicated than the [e3c-summer-worker/component](https://github.com/e3c-summer-worker/components) repo, since the packages depend on each other, but it doesn't matter.

The main goals of making this repo was to see if the following was feasible:

- A GH Workflow that automatically makes a new PR when a commit to main has a new changeset. This PR will update versions automatically, as well as the yarn dependencies.
- the GH workflow will also automatically publish the packcages when a new version is created.

This means, whether or not the commit is from a PR merge or a naive push to main, the PR with the new versions will be created, which we can then merge to main, automatically updating all the versions.
