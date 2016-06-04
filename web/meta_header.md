---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
meta:header
-----------

* Description: <none>
* Usage:

  * `meta:header [--dry-run] [--no-local]`

The <info>meta:header</info> command ensures that headers are present
in files matching the given filter in the current git repository.

Supported Files:
    - php
    - js
    - css
    - twig

If you don't want certain files or directories to be updated,
you can configure which paths must be excluded.

Add the following to your local <comment>.gush.yml</comment> file.
<comment>
meta-exclude:
    - lib/      # excludes all the files in the lib/ directory
    - meta/*.js # excludes all the js-files in the meta-folder
</comment>

Each value in the "meta-exclude" is either a Glob or complete regexp pattern
which excludes the path from being updated by the meta:header command.

Please keep the following in mind with using patterns:

- paths are relative to your repository root-folder
- patterns are case-sensitive (unless you use regexp with the 'i' (insensitive) flag like "/lib\//i")
- patterns are applied to both directories and file-names (end related patterns with '/' to restrict to directories)

For more information on using the paths see: http://symfony.com/doc/current/components/finder.html#path

<info>Tip:</info> If you are not sure your patterns are correct, run the meta:header command with
<comment>--dry-run</comment> to get a list of files that 'would' have been updated.


### Options:

**dry-run:**

* Name: `--dry-run`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Do not change anything, output files
* Default: `false`

**no-local:**

* Name: `--no-local`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Do not use the local meta header if it is available
* Default: `false`
{% endblock %}