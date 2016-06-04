---
title: Gush: Rapid workflow for project maintainers and contributors
---
pull-request:merge
------------------

* Description: Merges the pull request given
* Usage:

  * `pull-request:merge [--no-comments] [-ff|--fast-forward] [--squash] [--force-squash] [--switch SWITCH] [--] <pr_number> [<pr_type>]`

The <info>pull-request:merge</info> command merges the given pull request:

    <info>$ gush pull-request:merge 12</info>

Optionally you can prefix the merge title with a type like: bug, feature or anything you like.
<comment>Using a type makes it easier to search for a such a PR-type in your git history.</comment>

    <info>$ gush pull-request:merge 12 bug</info>

If there are many unrelated commits (like cs fixes) you can squash all the commits in the
pull-request into one big commit using:

    <info>$ gush pull-request:merge --squash 12</info>

This will use the message-body and author of the first commit in the pull-request.

<comment>Note:</comment> Squashing a PR requires that all the commits in the pull-request were done by one author.
You can overwrite this behaviour with <comment>--force-squash</comment>

If the pull request was opened against the master branch as target, but you rather want to merge it into another branch,
like "development" you can use <comment>--switch</comment> to change the base when merging.

<comment>This will only merge the commits that are in the source branch but not in the original target branch!</comment>

    <info>$ gush pull-request:merge --switch=development 12</info>

Pull-requests are merged as non fast-forward, which means a merge-commit (or merge bubble) is
created when merging. But sometimes you would rather want to merge without creating a merge bubble.

To merge a pull-request as fast-forward (no merge-commit) use the <comment>--fast-forward</comment>
option. Note that no merge-message is available and the changes are merged as if they were created in
the target branch directly!

    <info>$ gush pull-request:merge --fast-forward 12</info>

### Arguments:

**pr_number:**

* Name: pr_number
* Is required: yes
* Is array: no
* Description: Pull Request number
* Default: `NULL`

**pr_type:**

* Name: pr_type
* Is required: no
* Is array: no
* Description: Pull Request type eg. bug, feature (default is merge)
* Default: `NULL`

### Options:

**no-comments:**

* Name: `--no-comments`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Avoid adding PR comments to the merge commit message
* Default: `false`

**fast-forward:**

* Name: `--fast-forward`
* Shortcut: `-ff`
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Merge pull-request using fast forward (no merge commit will be created)
* Default: `false`

**squash:**

* Name: `--squash`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Squash the PR before merging
* Default: `false`

**force-squash:**

* Name: `--force-squash`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Force squashing the PR, even if there are multiple authors (this will implicitly use --squash)
* Default: `false`

**switch:**

* Name: `--switch`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Switch the base of the pull request before merging
* Default: `NULL`
