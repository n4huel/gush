---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
issue:show
----------

* Description: Shows given issue
* Usage:

  * `issue:show [--with-comments] [--] [<issue>]`

The <info>issue:show</info> command shows issue details for either the current or the given organization
and repo:

    <info>$ gush issue:show 60</info>

You can also call the command without the issue argument to pick up the current issue from the branch name:

    <info>$ gush issue:show</info>


### Arguments:

**issue:**

* Name: issue
* Is required: no
* Is array: no
* Description: Issue number
* Default: `NULL`

### Options:

**with-comments:**

* Name: `--with-comments`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Display comments from this issue
* Default: `false`
{% endblock %}