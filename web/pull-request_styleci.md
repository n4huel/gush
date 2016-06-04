---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:styleci
--------------------

* Description: Apply StyleCI patches on given PR
* Usage:

  * `pull-request:styleci <pr_number>`

The <info>pull-request:styleci</info> command applies StyleCI patches on given PR:

    <info>$ gush pull-request:styleci 12</info>


### Arguments:

**pr_number:**

* Name: pr_number
* Is required: yes
* Is array: no
* Description: PR number
* Default: `NULL`
{% endblock %}