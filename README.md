# Basic Git Cheatsheets

### Checking the Status of a Git Repository
The **git status** command is used within a **Git repository** to displays the state of the working directory and the staging area.
The output of git status can vary widely, and it often includes helpful messages to direct the user to manage their repository. For example, git status will show the user the files they would commit by running git commit and the files they could commit by running git add before running git commit.
#### Example git status command
<ul></ul> `$ Edit example.py `
<ul></ul> $ git status
<ul></ul> example.py is listed under "Changes not staged for commit"
<ul></ul>git add example.py
</ul>$ git status
</ul>example.py is listed under "Changes to be committed"
<ul></ul>$ git commit
<ul></ul>$ git status
<ul></ul>nothing to commit (working directory clean)

<ul></ul> The first status output will show the file as unstaged. The git add action will be reflected in the second git status, and the final status output will tell you that there is nothing to commit—the working directory matches the most recent commit. Some Git commands (e.g., git merge) require the working directory to be clean so that you don't accidentally overwrite changes.
