---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:switch-base
------------------------

* Description: Switch the base of the PR to another one
* Usage:

  * `pull-request:switch-base [--force-new-pr] [--] <pr_number> [<base_branch>]`

The <info>pull-request:switch-base</info> command switches the base of the given pull request
to the given base. This will preserve all commits made after the current base.

    <info>$ gush pull-request:switch-base 12 2.3</info>

When switching the base is not supported by the used adapter, a new pull request is
created instead. You can overwrite this behaviour with <comment>--force-new-pr</comment> to create
a new pull request (even if the adapter supports switching).

    <info>$ gush pull-request:switch-base --force-new-pr 12 2.3</info>

<fg=yellow;options=bold>To ensure a proper rebase process it's advised to make sure the
pull-request branch is up-to-date with the current base!</>

### Arguments:

**pr_number:**

* Name: pr_number
* Is required: yes
* Is array: no
* Description: PR number to be switched
* Default: `NULL`

**base_branch:**

* Name: base_branch
* Is required: no
* Is array: no
* Description: Name of the new base branch to switch the PR to
* Default: `'master'`

### Options:

**force-new-pr:**

* Name: `--force-new-pr`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Create a new PR, even when the used adapter supports switching the base
* Default: `false`
{% endblock %}