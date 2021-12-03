# changeset-actions-test

This is a repo to test out the [Changesets/action](https://github.com/changesets/action) bot.
The repo should mirror the repo in the [e3c-summer-worker/component](https://github.com/e3c-summer-worker/components) repo.

I have two main goals of making this repo:

- I want a GH Workflow that automatically makes a new PR when a commit has a new changeset, with the new versions
  - It should be able to handle multiple changesets in a single commit
  - Thus, when a PR is merged with a changeset, it will create the versioning PR
  - Also, when you naively push to the main branch, it will also create a versioning PR
