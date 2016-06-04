---
layout: docu-page
full_title: "Gush: Rapid workflow for project maintainers and contributors"
---
{% block content %}
branch:merge
------------

* Description: Merges the remote branch into the given branch
* Usage:

  * `branch:merge [--message [MESSAGE]] [--no-log] [-ff|--fast-forward] [--squash] [--force-squash] [--ignore-workflow] [--source-org SOURCE-ORG] [--source-repo SOURCE-REPO] [--] <source_branch> <target_branch>`

The <info>branch:merge</info> command merges the given source branch into the target branch:

    <info>$ gush branch:merge 2.3 2.7</info>

The default merge message is <comment>Merge branch '{{ source }}' into {{ target }}\n{{ commits_summary }}</>

But you can change this by using the <comment>--message</> option:

    <info>$ gush branch:merge 2.3 2.7 --message="Merge upstream changes into master"</info>

The message is appended with a commits summary, to disable this use the <comment>--no-log</> option.

    <info>$ gush branch:merge 2.3 2.7 --no-log --message="Merge upstream changes into master"</info>

Squashing commits
-----------------

If there are many unrelated commits (like cs fixes) you can squash all the commits of the source branch
into one big commit using:

    <info>$ gush branch:merge --squash 2.3 2.7</info>

This will use the message-body and author of the first commit in the source branch.

<comment>Note:</> Squashing the sources branch requires that all the commits in the source branch
were done by one author. You can overwrite this behaviour with <comment>--force-squash</>

Merge workflow
--------------

Note: The merge workflow it only applied for merges performed with the branch:merge,
pull-requests and using Git directly doesn't use the configured workflow.

To prevent merging a newer version into an older one, the branch:merge always
checks if the merge is correct according to your (teams) workflow.

The default workflow checks if the source branch and target branch are
versions, then checks if the source branch is lower then the target branch (merging
bug fixes into a new version). And allows to merge "develop" into "master" (but not the
other way around).

If you have a more complex workflow you can configure this in your local
<comment>.gush.yml</comment> file.

Gush already supports a number of standard workflows, but creating your own is also possible.

The merge_workflow.validation configuration is build is follow:

  * "preset": use a standardized workflow, e.g: "git-flow", "semver" or "none".
  * "branches": set a more specific validation (on top of the preset), each entry is a
    key (source branch) and the value an array of allowed target branches.
  * "unknown_branch_policy": what must be done when no rule matches, e.g: allow-merge, deny-merge.

<warning>To prevent casting the branch name to a normalized number, always use quotes for a numeric
branch name like '2.0'.</warning>

Note that "branches" are validated after "preset", to only use "branches" set "none" as the "preset" value.

Default workflow (allows to merge an older version into a newer one, but not the other way around,
and allows any other merge):
<comment>
merge_workflow:
    validation:
        preset: semver
        branches: []
</comment>

GitFlow as described in http://nvie.com/posts/a-successful-git-branching-model/:
<comment>
merge_workflow:
    validation:
        preset: git-flow
</comment>

Semantic version (allows to merge an older version into a newer once, but not the other way around):
<comment>
merge_workflow:
    validation:
        preset: semver
</comment>

Fully custom workflow validation:
<comment>
merge_workflow:
    validation:
        preset: none
        unknown_branch_policy: allow-merge
        branches:
            develop: [master]
            stable: [develop]
            '2.3': ['2.4']
            '2.4': ['2.5']
            '2.5': ['master']
</comment>

If you want to skip the workflow for the current merge use the <comment>--ignore-workflow</> option.

    <info>$ gush branch:merge --ignore-workflow 2.7 2.3</info>


### Arguments:

**source_branch:**

* Name: source_branch
* Is required: yes
* Is array: no
* Description: Source branch to merge from
* Default: `NULL`

**target_branch:**

* Name: target_branch
* Is required: yes
* Is array: no
* Description: Target branch to merge to
* Default: `NULL`

### Options:

**message:**

* Name: `--message`
* Shortcut: <none>
* Accept value: yes
* Is value required: no
* Is multiple: no
* Description: Optional message to use for the merge commit, default is: Merge branch '{{source}}' into {{target}}
* Default: `NULL`

**no-log:**

* Name: `--no-log`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Do not append a commit summary log
* Default: `false`

**fast-forward:**

* Name: `--fast-forward`
* Shortcut: `-ff`
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Merge branch using fast forward (no merge commit will be created)
* Default: `false`

**squash:**

* Name: `--squash`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Squash the commits before merging
* Default: `false`

**force-squash:**

* Name: `--force-squash`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Force squashing the commits, even if there are multiple authors (this will implicitly use --squash)
* Default: `false`

**ignore-workflow:**

* Name: `--ignore-workflow`
* Shortcut: <none>
* Accept value: no
* Is value required: no
* Is multiple: no
* Description: Ignore merge workflow configuration
* Default: `false`

**source-org:**

* Name: `--source-org`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Source Organization - source organization name (defaults to current organization)
* Default: `NULL`

**source-repo:**

* Name: `--source-repo`
* Shortcut: <none>
* Accept value: yes
* Is value required: yes
* Is multiple: no
* Description: Source Repository - source Repository name (defaults to current repository)
* Default: `NULL`
{% endblock %}