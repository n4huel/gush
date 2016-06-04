---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
release:create
--------------

* Description: Create a new Release
* Usage:

  * `release:create [--target-commitish TARGET-COMMITISH] [--name NAME] [--body BODY] [--draft] [--prerelease] [--asset-file ASSET-FILE] [--asset-name ASSET-NAME] [--asset-content-type ASSET-CONTENT-TYPE] [--replace] [--] <tag>`

The <info>release:create</info> command creates a release:

    <info>$ gush release:create</info>


### Arguments:

**tag:**

* Name: tag
* Is required: yes
* Is array: no
* Description: Tag of the release
* Default: `NULL`

### Options:

**target-commitish:**

* Name: `--target-commitish`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Commitish/ref to create the tag from
* Default: `NULL`

**name:**

* Name: `--name`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Name of the release
* Default: `NULL`

**body:**

* Name: `--body`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Description of the release
* Default: `NULL`

**draft:**

* Name: `--draft`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Specify to create an unpublished release
* Default: `false`

**prerelease:**

* Name: `--prerelease`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Specify to create a pre-release, omit for full release
* Default: `false`

**asset-file:**

* Name: `--asset-file`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: yes
* Description: Assets to include in this release
* Default: `array ()`

**asset-name:**

* Name: `--asset-name`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: yes
* Description: Names corresponding to asset-files
* Default: `array ()`

**asset-content-type:**

* Name: `--asset-content-type`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: yes
* Description: Content types corresponding to asset-files (default: application/zip)
* Default: `array ()`

**replace:**

* Name: `--replace`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Replace any existing release with the same name
* Default: `false`
{% endblock %}