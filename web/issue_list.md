---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
issue:list
----------

* Description: List issues
* Usage:

  * `issue:list [--label LABEL] [--milestone MILESTONE] [--assignee ASSIGNEE] [--creator CREATOR] [--mentioned MENTIONED] [--state STATE] [--sort SORT] [--direction DIRECTION] [--type TYPE] [--since SINCE]`

The <info>issue:list</info> command lists issues from either the current or the given organization
and repository:

    <info>$ php issue:list</info>
    <info>$ php issue:list --creator=cordoval --sort=created --direction=desc --since="6 months ago"
    --type=pr</info>

All of the parameters provided by the github API are supported:

    https://developer.github.com/v3/issues/#list-issues-for-a-repository

With the addition of the <info>--type</info> option which enables you to filter show only pull-requests or only issues.


### Options:

**label:**

* Name: `--label`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: yes
* Description: <none>
* Default: `array ()`

**milestone:**

* Name: `--milestone`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: <none>
* Default: `NULL`

**assignee:**

* Name: `--assignee`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Username assignee. None for unassigned.
* Default: `NULL`

**creator:**

* Name: `--creator`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: The user that created the issue.
* Default: `NULL`

**mentioned:**

* Name: `--mentioned`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: The user mentioned in the issue.
* Default: `NULL`

**state:**

* Name: `--state`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Issue state (One of <comment>open</comment>, <comment>closed</comment>)
* Default: `NULL`

**sort:**

* Name: `--sort`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Sort issues by (One of <comment>created</comment>, <comment>updated</comment>)
* Default: `NULL`

**direction:**

* Name: `--direction`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Sort direction (One of <comment>asc</comment>, <comment>desc</comment>)
* Default: `NULL`

**type:**

* Name: `--type`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Issue type (One of <comment>pr</comment>, <comment>issue</comment>)
* Default: `NULL`

**since:**

* Name: `--since`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Only issues after this time are displayed.
* Default: `NULL`
{% endblock %}