---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
pull-request:create
-------------------

* Description: Launches a pull request
* Usage:

  * `pull-request:create [--base BASE] [--source-org SOURCE-ORG] [--source-repo SOURCE-REPO] [--source-branch SOURCE-BRANCH] [--title TITLE]`

The <info>pull-request:create</info> command is used to make a pull-request
against the configured organization and repository.

    <info>$ gush pull-request:create</info>

The remote branch to make the PR against can be specified with the
<comment>--base</comment> option, and the local organization / branch with the <comment>--source-org</comment> /
<comment>--source-branch</comment> options, when these options are omitted they are determined from the current
context.

    <info>$ gush pull-request:create --source-branch=my_branch --source-org=my_org --base=dev</info>

A pull-request template can be specified with the <info>template</info> option:

    <info>$ gush pull-request:create --template=symfony</info>

This will use the Symfony specific pull-request template, the full list of
available templates is displayed in the description of the <info>template</info>
option.

Note: The "custom" template is only supported when you have configured this in
your local <comment>.gush.yml</comment> file like:
<comment>
table-pr:
    bug_fix: ['Bug Fix?', no]
    new_feature: ['New Feature?', no]
    bc_breaks: ['BC Breaks?', no]
    deprecations: ['Deprecations?', no]
    tests_pass: ['Tests Pass?', no]
    fixed_tickets: ['Fixed Tickets', '']
    license: ['License', MIT]
</comment>

Each key in "table-pr" list is the name used internally by the command engine, you can choose any name
you like but note that "description" is preserved for internal usage and is not changeable
and you can only use underscores for separating words.

The value of each key is an array with "exactly two values" like ['the label', 'the default value'].

If you don't want to configure any fields at all use the following.
<comment>
table-pr: []
</comment>
<info>This will still ask the title and description, but no additional fields.</info>

When using a template you will be prompted to fill out the required parameters.


### Options:

**base:**

* Name: `--base`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Base Branch - remote branch name
* Default: `NULL`

**source-org:**

* Name: `--source-org`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Source Organization - source organization name (defaults to current)
* Default: `NULL`

**source-repo:**

* Name: `--source-repo`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Source Repository - source Repository name (defaults to current)
* Default: `NULL`

**source-branch:**

* Name: `--source-branch`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Source Branch - source branch name (defaults to current)
* Default: `NULL`

**title:**

* Name: `--title`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: PR Title
* Default: `NULL`
{% endblock %}