---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
issue:label:assign
------------------

* Description: Labels issues/pull requests
* Usage:

  * `issue:label:assign [--new] [--issues] [--pull-requests]`

The <info>issue:label:assign</info> command labels issue or pull requests for either the current or the given organization
and repo:

    <info>$ gush issue:label:assign</info>


### Options:

**new:**

* Name: `--new`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Get only new issues/pull requests
* Default: `false`

**issues:**

* Name: `--issues`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Get issues
* Default: `false`

**pull-requests:**

* Name: `--pull-requests`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Get pull requests
* Default: `false`
{% endblock %}