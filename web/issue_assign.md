---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
issue:assign
------------

* Description: Assigns an issue to a user
* Usage:

  * `issue:assign <issue_number> <username>`

The <info>issue:assign</info> command assigns an issue to a user:

    <info>$ gush issue:assign 3 cordoval</info>


### Arguments:

**issue_number:**

* Name: issue_number
* Is required: yes
* Is array: no
* Description: Number of the issue
* Default: `NULL`

**username:**

* Name: username
* Is required: yes
* Is array: no
* Description: Username of the assignee
* Default: `NULL`
{% endblock %}