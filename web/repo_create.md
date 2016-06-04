---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
repo:create
-----------

* Description: Creates a new repository
* Usage:

  * `repo:create [--private] [--no-init] [--target-org TARGET-ORG] [--] <name> [<description>] [<homepage>]`

The <info>repo:create</info> command creates a new repository:

    <info>$ gush repo:create my-package</info>

By default the repository will be created in your "personal" organization (your username)
to create the repository in a specific organization use the <comment>--target-org</> option.

    <info>$ gush repo:create --target-org=my-org my-package</info>

If you want to create a private repository (non open-source) use the <comment>--private</> option:

    <info>$ gush repo:create --private my-package</info>

Note: Private repositories may not be supported by the used adapter or only in paid/higher plans.

Last, if you don't want to initialize the repository (with an initial commit) use
the <comment>--no-init</> option:

    <info>$ gush repo:create --no-init my-package</info>

This will leave the repository empty, you need to push at least one commit
before any pull requests can be opened.

### Arguments:

**name:**

* Name: name
* Is required: yes
* Is array: no
* Description: Name of the new repository
* Default: `NULL`

**description:**

* Name: description
* Is required: no
* Is array: no
* Description: Repository description
* Default: `NULL`

**homepage:**

* Name: homepage
* Is required: no
* Is array: no
* Description: Repository homepage
* Default: `NULL`

### Options:

**private:**

* Name: `--private`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Make a private repository (may require a plan upgrade)
* Default: `false`

**no-init:**

* Name: `--no-init`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Create an empty repository instead of having an "initial commit"
* Default: `false`

**target-org:**

* Name: `--target-org`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Target organization (defaults to your username)
* Default: `NULL`
{% endblock %}