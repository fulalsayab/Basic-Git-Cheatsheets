# Basic Git Cheatsheets

### Checking the Status of a Git Repository
The **git status** command is used within a **Git repository** to displays the state of the working directory and the staging area.
The output of git status can vary widely, and it often includes helpful messages to direct the user to manage their repository. For example, git status will show the user the files they would commit by running git commit and the files they could commit by running git add before running git commit.
#### Example git status command
```
 $ Edit example.py
 $ git status
 example.py is listed under "Changes not staged for commit"
 git add example.py
 $ git status
 example.py is listed under "Changes to be committed"
 $ git commit
 $ git status
 nothing to commit (working directory clean)
 ```
  The first status output will show the file as unstaged. The git add action will be reflected in the second git status, and the final status output will tell you that there is nothing to commit—the working directory matches the most recent commit. Some Git commands (e.g., git merge) require the working directory to be clean so that you don't accidentally overwrite changes.
