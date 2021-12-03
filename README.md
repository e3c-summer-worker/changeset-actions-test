# changeset-actions-test

This is a repo to test out the [Changesets/action](https://github.com/changesets/action) GH action, so I can use automate versioning in the [Components](https://github.com/e3c-summer-worker/components) repo.

**NOTE**: The Changeset/actions bot requires a Github Personal Access token to work. I created one for it to use (go to [Settings -> Tokens](https://github.com/settings/tokens)), but for security reasons (and because this repo is meant to be temporary), I've made it expire on March 3, 2022.

If you want to test the repo after that date, please make a new PAT and update the actions secrets [at the Repo Settings -> Secrets](https://github.com/e3c-summer-worker/changeset-actions-test/settings/secrets/actions).

The contents are based off of [monorepo-release-changesets](https://github.com/azu/monorepo-release-changesets), but their versioning system is a bit unnecessary for me. It's a bit more complicated than the [e3c-summer-worker/component](https://github.com/e3c-summer-worker/components) repo, since the packages depend on each other.

I have two main goals of making this repo:

- I want a GH Workflow that automatically makes a new PR when a commit has a new changeset, with the new versions
  - It should be able to handle multiple changesets in a single commit
  - Thus, when a PR is merged with a changeset, it will create the versioning PR
  - Also, when you naively push to the main branch, it will also create a versioning PR
