---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:assign
-------------------

* Description: Assigns a pull-request to a user
* Usage:

  * `pull-request:assign <pr_number> <username>`

The <info>pull-request:assign</info> command assigns a pull request to a user:

    <info>$ gush pull-request:assign 3 cordoval</info>


### Arguments:

**pr_number:**

* Name: pr_number
* Is required: yes
* Is array: no
* Description: Number of the pull request
* Default: `NULL`

**username:**

* Name: username
* Is required: yes
* Is array: no
* Description: Username of the assignee
* Default: `NULL`
{% endblock %}