---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
issue:take
----------

* Description: Takes an issue
* Usage:

  * `issue:take <issue_number> [<base_branch>]`

The <info>issue:take</info> command takes an issue from the issue-tracker:

    <info>$ gush issue:take 3</info>

In practice this will add the organization as remote (if not registered already), then
<comment>git checkout org/base_branch</> and create a new branch that is equal to the issue-number + title.

When no "base_branch" argument is provided the "base" is fetched from your local .gush.yml config-file,
if no base is set "master" is used.

Note: If you don't use "master" as your default base branch you can set the default "base" in your
local .gush.yml config-file:

<comment>
base: develop
</comment>

After you are done you can open a new pull-request using the <info>$ gush pull-request:create</info> command.


### Arguments:

**issue_number:**

* Name: issue_number
* Is required: yes
* Is array: no
* Description: Number of the issue
* Default: `NULL`

**base_branch:**

* Name: base_branch
* Is required: no
* Is array: no
* Description: Name of the base branch to checkout from
* Default: `NULL`
{% endblock %}