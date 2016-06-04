---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
issue:create
------------

* Description: Creates an issue
* Usage:

  * `issue:create [--title TITLE] [--body BODY]`

The <info>issue:create</info> command creates a new issue for either the current or the given organization
and repository:

    <info>$ gush issue:create</info>


### Options:

**title:**

* Name: `--title`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Issue Title
* Default: `NULL`

**body:**

* Name: `--body`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Issue Body
* Default: `NULL`
{% endblock %}