---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:checkout
---------------------

* Description: Checks out a pull request as local branch
* Usage:

  * `pull-request:checkout <pr_number>`

The <info>pull-request:checkout</info> command is used to check a pull-request out from the organization.

When the branch already exists Gush will check if the remote-upstream is the same
as the source organization of the pull-request and check out the local branch instead.


### Arguments:

**pr_number:**

* Name: pr_number
* Is required: yes
* Is array: no
* Description: Pull Request number to be checked-out
* Default: `NULL`
{% endblock %}