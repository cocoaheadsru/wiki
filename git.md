# Working with Git

These guidelines applied to **all** CocoaHeads Russia projects.

## General

We use [GitFlow](http://nvie.com/posts/a-successful-git-branching-model/) approach in our projects.

![GitFlow](/resources/images/gitflow.png)

## Branching

We use [Trello](https://trello.com) for task managements and [this hook](/resporces/scripts/prepare-commit-msg) for git integration with Trello

**How it works?**

Each git brach name should match the following pattern `task/TRELLO_TASK_ID/task-description` **(e.g `task/D84aPyrz/create-models`)**. Hook looks for task id and push it to your commit message. You should write task id once in your branch name.

**To apply hook**

- Place it in `{PROJECT_FOLDER_PATH}/.git/hooks` folder
- Change its access permitions to `755`

<!-- Separate code from list -->

    cd {PROJECT_FOLDER_PATH}/.git/hooks
    chmod 755 prepare-commit-msg

## Commit

- Use only English for commit comments
- Comments must start from verb and describe main changes **(e.g. Fixed GitHub authorization bug, Added User model)**
- Use separate commit for updating project dependencies
- Before commit go through all changes and make sure that there are no:
  - commented code
  - unnecessary logging
  - code belonging to another task
- Make sure that code compiles

All `git commit` go through code review. Reviewers take common responsibility with commit author for code quality.

### Merge

General rules

- **For `develop` and below branches**. Commit can be merged if there are no warnings except of *TODO* or *FIXME*
- **For `master` branch** — if there are no warning at all
- Empty commits (whitespaces, code formatting without changes) won't be merged, to revert use `discard hunk`

## Pull Requests

Pull request must include:

- Trello task's name and link
- Full explanation what was done
- What reviewers need to pay additional attention for and how your code can be tested
- If there are any connected Trello tasks add them also
- If you split pull request add stage-by-stage list of changes

**You can use [this PR template](/resources/files/pull_request_template.md)**.

### PR Example