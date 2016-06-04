---
title: Gush: Rapid workflow for project maintainers and contributors
---
branch:remote:add
-----------------

* Description: Adds a remote with url used from adapter
* Usage:

  * `branch:remote:add [<other_organization>] [<other_repository>] [<remote>]`

The <info>branch:remote:add</info> command adds a remote with a url provided by the adapter:

    <info>$ gush branch:remote:add sstok gush</info>

<fg=yellow;options=bold>Warning! Any existing remote with the same name will be overwritten!</>

### Arguments:

**other_organization:**

* Name: other_organization
* Is required: no
* Is array: no
* Description: Organization or username the remote will point to
* Default: `NULL`

**other_repository:**

* Name: other_repository
* Is required: no
* Is array: no
* Description: Repository-name the remote will point to
* Default: `NULL`

**remote:**

* Name: remote
* Is required: no
* Is array: no
* Description: Remote name. When not provided the other_organization is used as remote-name
* Default: `NULL`
