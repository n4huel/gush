---
title: Gush: Rapid workflow for project maintainers and contributors
---
core:update
-----------

* Description: Updates the application.
* Usage:

  * `core:update [-p|--pre] [-r|--redo] [-u|--upgrade]`

Updates the application.

### Options:

**pre:**

* Name: `--pre`
* Shortcut: `-p`
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Allow pre-release updates.
* Default: `false`

**redo:**

* Name: `--redo`
* Shortcut: `-r`
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Redownload update if already using current version.
* Default: `false`

**upgrade:**

* Name: `--upgrade`
* Shortcut: `-u`
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Upgrade to next major release, if available.
* Default: `false`
