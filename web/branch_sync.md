---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
branch:sync
-----------

* Description: Syncs local branch with its upstream version
* Usage:

  * `branch:sync [<branch_name>] [<remote>]`

The <info>branch:sync</info> command syncs local branch with it's origin version:

    <info>$ gush branch:sync develop origin</info>


### Arguments:

**branch_name:**

* Name: branch_name
* Is required: no
* Is array: no
* Description: Branch name to sync
* Default: `NULL`

**remote:**

* Name: remote
* Is required: no
* Is array: no
* Description: Git remote to pull from (defaults to origin)
* Default: `'origin'`
{% endblock %}