---
title: Gush: Rapid workflow for project maintainers and contributors
---
branch:fork
-----------

* Description: Forks current upstream repository
* Usage:

  * `branch:fork [<target_organization>]`

The <info>branch:fork</info> command forks the upstream (defined by --org and --repo) repository
and adds the remote to your local Git configuration:

    <info>$ gush branch:fork</info>

By default this will fork the upstream to your username-organization, to fork into a different
target-organization use the following instead (where my-other-org is the name of the organization
you want to fork to):

    <info>$ gush branch:fork my-other-org</info>


### Arguments:

**target_organization:**

* Name: target_organization
* Is required: no
* Is array: no
* Description: Target organization to create the fork in. (Defaults to your username)
* Default: `NULL`
