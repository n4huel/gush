---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
help
----

* Description: Displays help for a command
* Usage:

  * `help [--xml] [--format FORMAT] [--raw] [--] [<command_name>]`

The <info>help</info> command displays help for a given command:

  <info>php gush.phar help list</info>

You can also output the help in other formats by using the <comment>--format</comment> option:

  <info>php gush.phar help --format=xml list</info>

To display the list of available commands, please use the <info>list</info> command.

### Arguments:

**command_name:**

* Name: command_name
* Is required: no
* Is array: no
* Description: The command name
* Default: `'help'`

### Options:

**xml:**

* Name: `--xml`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: To output help as XML
* Default: `false`

**format:**

* Name: `--format`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: The output format (txt, xml, json, or md)
* Default: `'txt'`

**raw:**

* Name: `--raw`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: To output raw command help
* Default: `false`
{% endblock %}