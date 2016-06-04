---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:semver
-------------------

* Description: Provides information about the semver version of a pull-request
* Usage:

  * `pull-request:semver [--major] [--minor] [--patch] [--] <pr_number>`

The <info>pull-request:semver</info> command provides information about semver version of a pull request:

    <info>$ gush pull-request:semver 12</info>


### Arguments:

**pr_number:**

* Name: pr_number
* Is required: yes
* Is array: no
* Description: Pull Request number
* Default: `NULL`

### Options:

**major:**

* Name: `--major`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Conveys it is a major feature
* Default: `false`

**minor:**

* Name: `--minor`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Conveys it is a minor feature
* Default: `false`

**patch:**

* Name: `--patch`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Conveys it is a patch
* Default: `false`
{% endblock %}