---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
issue:close
-----------

* Description: Closes an issue
* Usage:

  * `issue:close [-m|--message MESSAGE] [--] <issue_number>`

The <info>issue:close</info> command closes an issue for either the current or the given organization
and repository:

    <info>$ gush issue:close 12 -m"let's try to keep it low profile guys."</info>


### Arguments:

**issue_number:**

* Name: issue_number
* Is required: yes
* Is array: no
* Description: Issue number to be closed
* Default: `NULL`

### Options:

**message:**

* Name: `--message`
* Shortcut: `-m`
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Closing comment
* Default: `NULL`
{% endblock %}