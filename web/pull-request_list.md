---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:list
-----------------

* Description: Lists all available pull requests
* Usage:

  * `pull-request:list [--state STATE]`

The <info>pull-request:list</info> command lists all the pull requests:

    <info>$ gush pull-request:list</info>


### Options:

**state:**

* Name: `--state`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: For a list of available states, please refer to the adapter documentation
* Default: `NULL`
{% endblock %}