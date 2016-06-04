---
title: Gush: Rapid workflow for project maintainers and contributors
---
issue:copy
----------

* Description: Copy issue
* Usage:

  * `issue:copy [-ta|--target-adapter [TARGET-ADAPTER]] [--prefix PREFIX] [--close] [--with-comments] [--] <issue_number> <target_username> <target_repository>`

The <info>issue:copy</info> command moves an issue from one repository to another


### Arguments:

**issue_number:**

* Name: issue_number
* Is required: yes
* Is array: no
* Description: Issue number to move
* Default: `NULL`

**target_username:**

* Name: target_username
* Is required: yes
* Is array: no
* Description: Target username or organization
* Default: `NULL`

**target_repository:**

* Name: target_repository
* Is required: yes
* Is array: no
* Description: Target repository
* Default: `NULL`

### Options:

**target-adapter:**

* Name: `--target-adapter`
* Shortcut: `-ta`
* Accept value: yes
* Is value required: no
* Is multiple: no
* Description: Adapter-name of the target issue-manager
* Default: `NULL`

**prefix:**

* Name: `--prefix`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Prefix for the issue title
* Default: `NULL`

**close:**

* Name: `--close`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Close original issue
* Default: `false`

**with-comments:**

* Name: `--with-comments`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Also copy comments
* Default: `false`
