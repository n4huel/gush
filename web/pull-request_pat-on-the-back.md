---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:pat-on-the-back
----------------------------

* Description: Gives a pat on the back to a PR's author
* Usage:

  * `pull-request:pat-on-the-back <pr_number>`

The <info>pull-request:pat-on-the-back</info> command gives a pat on the back to a PR's author with a random template:

    <info>$ gush pull-request:pat-on-the-back 12</info>


### Arguments:

**pr_number:**

* Name: pr_number
* Is required: yes
* Is array: no
* Description: Pull request number
* Default: `NULL`
{% endblock %}