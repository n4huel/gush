---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:squash
-------------------

* Description: Squashes all commits of a pull request
* Usage:

  * `pull-request:squash [--no-local-sync] [--] <pr_number>`

The <info>pull-request:squash</info> command squashes all commits of a pull-request:

    <info>$ gush pull-request:squash 12</info>

Make sure you are the pull-requests\'s source-branch repository owner
or have been granted push access to the repository.

Note: This will squash all commits in the pull-request and (when a local branch exists with
the same name) sync your local source branch with the squashed version.
You can skip this sync-process using the <comment>--no-local-sync</> option.

### Arguments:

**pr_number:**

* Name: pr_number
* Is required: yes
* Is array: no
* Description: pull-request number to squash
* Default: `NULL`

### Options:

**no-local-sync:**

* Name: `--no-local-sync`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Do not sync the local branch with the squashed version
* Default: `false`
{% endblock %}