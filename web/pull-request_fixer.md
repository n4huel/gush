---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:fixer
------------------

* Description: Run cs-fixer and commits fixes
* Usage:

  * `pull-request:fixer [<fixer_line>]`

The <info>pull-request:fixer</info> runs the coding style fixer and commits fix:

    <info>$ gush pull-request:fixer</info>


### Arguments:

**fixer_line:**

* Name: fixer_line
* Is required: no
* Is array: no
* Description: Custom fixer command
* Default: `'php-cs-fixer fix .'`
{% endblock %}