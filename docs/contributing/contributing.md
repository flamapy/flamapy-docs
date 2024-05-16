---
layout: default
title: Contributing
has_children: true
nav_order: 6
---

# Contributing
{: .no_toc }

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

## I want to contribute to the project. What should I do?

1. Find one issue you want to resolve. Make sure nobody else is working on such issue.
2. Follow the [Development guide](https://flamapy.github.io/docs/jekyll/2022-06-12-4-development.html) to set up the project. Consider you will have to fork the project you want to contribute to.
3. Create a new [branch](#how-should-i-name-my-branches) from develop in your forked project.
```bash
git branch new-branch develop
```
4. Make an [empty commit](#first-commit) on this branch and push.
```bash
git commit -m 'message' --allow-empty
git push -u origin new-branch
```

5. Create a PR with this empty commit, from your new branch, to base repository's develop branch. This PR's name must end with a keyword such as "solves" or "fixes" followed by the issue it solves (e.g., solves #115)
6. From this, any change you commit and push to your branch will be added to the PR. Keep [committing](#how-should-i-commit) until you finish developing your contribution and mention a maintainer so they can revise it. Check [this](#what-do-i-have-to-do-to-get-my-request-accepted) to know the requisites to get you request accepted.

## What can I contribute to?

You can contribute to any of the issues in any project.

## How should I name my branches?

Branches should follow a &lt;token&gt;-&lt;short-descriptive-name&gt; structure, where tokens can be such as:

- **chore**: Improvement on project maintenance or administration, such as dependencies updates.
- **docs**: Documentation creation or update.
- **feature**: New features added to the project.
- **fix/hotfix/patch**: Correction of bugs and errors.
- **refactor**: Improvement of already written code, with no changes on functionality.
- **test**: Addition or updates of tests to features.

## How should I commit?

Commits should be as **descriptive** and **atomic** as possible. However, commits collaborators make on their PRs will not be logged, as they will always be squashed.

For this reason, you will not have to worry much about commit messages following strict guidelines. Just see your commit history as a log for both maintainers and you to know the progress of the work.

### First commit

A first and mandatory commit has to be done, as mentioned before, to create the PR. This commit should contain a brief description of the remaining work.


## I found an error while working in a project. What should I do?

### The error found is outside the scope of my work.

1. Make sure it is an actual error and not a bad interaction between your code and the rest of the project.
2. [Open an issue](#how-and-when-can-i-open-a-new-issue) to keep track of the error.
3. You can assign the issue yourself if you either want to fix the error or need to do so for your code to work. If you want to fix that new issue, you SHOULD do it from a different PR. If it is impossible or too hard to separately fix it, fix the error on your already open PR, but you MUST clarify which commits are part of this new issue so maintainers know it when squashing.

### The error found comes from my own code.

* Fix it as soon as possible to prevent it from scaling.

## How and when can I open a new issue?

You can open an issue any time you find a bug or an idea to implement in a project. Whatever the reason is, issues will keep track of the remaining and finished tasks in projects. To keep the issues environment as efficient as possible, please consider the following practices:

* Provide a descriptive short title. Use description to give more in-depth details.
* Use labels to make your issues easier to filter.
* For bugs, try to find and mention the author of the code which is failing.
* For bugs, include as many details as possible to make them replicable and testable.
* Keep your notifications on so you know about mentions or comments on your issues.

## What do I have to do to get my request accepted?

### Mandatory conditions

* Your code must work and provide a solution to its correspondent issues.
* **pytest** command must return no errors.
* Code quality commands **prospector** and **mypy flamapy** must return no messages.

### Recommendations and good practices

These practices are not mandatory, but consider that highly messy contributions can be rejected. They also make it easier for maintainers to revise your requests, allowing them to give you feedback instead of just rejecting your contribution.

#### Descriptive pull requests

* Keep your commits [atomic](#atomic-commits) and [descriptive](#descriptive-commit-messages).
* You PR should end up looking like a history of concurrent descriptive commits that add up functionality until the issue is resolved.

#### Clean code

* Modularize your code with descriptive function names.
* Comment your code, but do not overdo it.
* Keep your lines short and readable.
* Use descriptive variable names.

#### Testing

* You should include functional testing to newly implemented features.