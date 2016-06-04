---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
core:alias
----------

* Description: Outputs help and alias snippet for wrapping gush on git
* Usage:

  * `core:alias [-s|--s]`

The <info>core:alias</info> outputs an alias snippet to wrap Gush on git:

    <info>$ gush core:alias -s</info>


### Options:

**s:**

* Name: `--s`
* Shortcut: `-s`
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Outputs only snippet
* Default: `false`
{% endblock %}