---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
release:remove
--------------

* Description: Removes a release
* Usage:

  * `release:remove <id>`

The <info>release:remove</info> command removes a given release:

    <info>$ gush release:remove 3</info>


### Arguments:

**id:**

* Name: id
* Is required: yes
* Is array: no
* Description: ID of the release
* Default: `NULL`
{% endblock %}