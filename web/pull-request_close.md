---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:close
------------------

* Description: Closes a pull request
* Usage:

  * `pull-request:close [-m|--message MESSAGE] [--] <pr_number>`

The <info>pull-request:close</info> command closes a Pull Request for either the current or the given organization
and repository:

    <info>$ gush pull-request:close 12 -m"let's try to keep it low profile guys."</info>


### Arguments:

**pr_number:**

* Name: pr_number
* Is required: yes
* Is array: no
* Description: Pull Request number to be closed
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