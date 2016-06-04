---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
branch:changelog
----------------

* Description: Reports what got fixed or closed since last release on the given branch
* Usage:

  * `branch:changelog [-s|--search SEARCH] [--] [<branch>]`

Reports what got fixed or closed since the last release on the given branch.

    <info>$ gush branch:changelog</info>

This command will search all the commits in the given branch (that were made after the last tag)
and will try to extract the issue numbers from the message. To only match a precise pattern, use the
<comment>--search</comment> option to specify one or multiple regex-patterns (with delimiters and flags).

For example, if your issues are prefixed with "JIRA-" or "DC-", use the following:

    <info>$ gush branch:changelog --search="{JIRA-(?P<id>[0-9]+)}i" --search="{DC-(?P<id>[0-9]+)}i"</info>

Note: It's important the regex has a "named capturing group" like <comment>(?P<id>[0-9]+)</comment>.
This named group must (only) match the issue number and nothing else.

To learn more about composing your own regex patterns see:
http://php.net/manual/reference.pcre.pattern.syntax.php
http://www.regular-expressions.info/

### Arguments:

**branch:**

* Name: branch
* Is required: no
* Is array: no
* Description: Branch to look for tags in. When unspecified, the current branch is used
* Default: `NULL`

### Options:

**search:**

* Name: `--search`
* Shortcut: `-s`
* Accept value: yes
* Is value required: yes
* Is multiple: yes
* Description: Regex pattern to use for searching
* Default: `array (  0 => '/#(?P<id>[0-9]+)/i',)`
{% endblock %}