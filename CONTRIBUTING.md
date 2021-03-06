# Contributing to Exercism.io

First of all, **thank you** for helping with Exercism.io!

This contributing guide is specifically about contributing to the exercism.io website codebase.
For a guide to the project as a whole check out the [finding your way][finding-your-way] guide in the [docs][] repository.

# Table of Contents

* [Code of Conduct](#code-of-conduct)
* [Contributing](#contributing)
* [Submitting Code Changes](#submitting-code-changes)
    - [Git Workflow](#git-workflow)
    - [Issues](#issues)
    - [Good First Patch](#good-first-patch)
    - [Style (Ruby)](#style-ruby)
    - [Style (JavaScript/CSS)](#style-js-css)
    - [Pull Requests](#pull-requests)
* [Roadmap](#roadmap)

## Code of Conduct

Help us keep exercism welcoming. Please read and abide by the [Code of Conduct][coc].

## Submitting Code Changes

If you're new to contributing to open source on GitHub, this next section should help you get started.
If you get stuck, open an issue to ask us for help and we'll get you sorted out (and improve these instructions).

See the [Setting up Local Development guide][local-dev-env] for more information about how to run exercism.io locally.

### Git Workflow

1. Fork and clone.
1. Add the upstream exercism.io repository as a new remote to your clone.
   `git remote add upstream https://github.com/exercism/exercism.io.git`
1. Create a new branch
   `git checkout -b name-of-branch`
1. Commit and push as usual on your branch.
1. When you're ready to submit a pull request, rebase your branch onto
   the upstream master so that you can resolve any conflicts:
   `git fetch upstream && git rebase upstream/master`
   You may need to push with `--force` up to your branch after resolving conflicts.
1. When you've got everything solved, push up to your branch and send the pull request as usual.

### Issues

We keep track of bugs, enhancements and support requests in the repository using GitHub [issues][].

For higher-level discussions about the project as a whole check out the issues in the [discussions][] repository.

### Good First Patch

We're trying to label issues with "good first patch" if we think that these can be solved
without too much context about exercism.io's codebase or functionality. To find them, you
can do a [search][good-first-patch].

### Style (Ruby)

We use [Rubocop][rubocop] to enforce a few style-related conventions.
Run the command `rubocop` to check for any style violations before submitting pull requests.

### Style (JS/CSS)

If you have any JS or CSS changes, please run `cd frontend && lineman spec-ci` to check for any problems before submitting pull requests.

### Pull Requests

When submitting a pull request, sometimes we'll ask you to make changes before
we accept the patch.

Please do not close the first pull request and open a second one with these
changes. If you push more commits to a branch that you've opened a pull
request for, it automatically updates the pull request.

When the pull request is ready to be merged, you will probably be asked to [squash your commits][squash-commits].

As with adding more commits, you do not need to close your pull request and open a new one.
If you change the history (`rebase`, `squash`, `amend`), use `git push --force` to update the branch on your fork.
The pull request points to that branch, not to specific commits.

Here's a guide on [how to squash commits in a GitHub pull request][squash-commits].

### Deployment

After your pull request is merged, we [deploy][live-deployment] it. Deploys are
done periodically, and it is possible that you won't be able to see your changes
on the website right away.

## Roadmap

We are currently working on reimagining the Exercism user experience from the ground up.

For details, please see [exercism/discussions#113][roadmap].

[finding-your-way]: https://github.com/exercism/docs/blob/master/finding-your-way.md
[docs]: https://github.com/exercism/docs
[coc]: https://github.com/exercism/exercism.io/blob/master/CODE_OF_CONDUCT.md
[local-dev-env]: https://github.com/exercism/exercism.io/blob/master/docs/setting-up-local-development.md
[issues]: https://github.com/exercism/exercism.io/issues
[discussions]: https://github.com/exercism/discussions/issues
[good-first-patch]: https://github.com/exercism/exercism.io/labels/good%20first%20patch
[rubocop]: https://github.com/bbatsov/rubocop
[roadmap]: https://github.com/exercism/discussions/issues/113
[squash-commits]: http://blog.steveklabnik.com/posts/2012-11-08-how-to-squash-commits-in-a-github-pull-request
[live-deployment]: https://github.com/exercism/exercism.io/blob/master/docs/setting-up-local-development.md#live-deployment
