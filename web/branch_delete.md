---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
branch:delete
-------------

* Description: Deletes the current branch, or the branch with the given name
* Usage:

  * `branch:delete [--force] [--] [<branch_name>] [<organization>]`

The <info>branch:delete</info> command deletes the current or given remote branch on
the organization (defaults to username):

    <info>$ gush branch:delete</info>

Note: The "organization" argument defaults to your username (the forked repository) not
the organization you would normally provide using the --org option.

For security reasons it's not directly possible to delete the "master" branch,
use the <comment>--force</comment> option to force a delete, use with caution!

### Arguments:

**branch_name:**

* Name: branch_name
* Is required: no
* Is array: no
* Description: Optional branch name to delete
* Default: `NULL`

**organization:**

* Name: organization
* Is required: no
* Is array: no
* Description: Organization (defaults to username) where the branch will be deleted
* Default: `NULL`

### Options:

**force:**

* Name: `--force`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Attempts to delete the branch even when permissions detected are insufficient
* Default: `false`
{% endblock %}