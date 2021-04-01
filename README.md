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
  
 ### Initializing a Git Repository
The **git init** command creates or initializes a new Git project, or repository. It creates a .git folder with all the tools and data necessary to maintain versions. This command only needs to be used once per project to complete the initial setup. For instance, the code block sets up the home folder as a new git repository.
```
$ cd /home
$ git init
```
This command creates an empty Git repository - basically a .git directory with subdirectories for objects, refs/heads, refs/tags, and template files. 

### Displaying Differences with Git Diff
The **git diff filename** command will display the differences between the working directory and the staging area in one specific file. Use git diff filename before adding new content to ensure that you are making the changes you expect.
#### Example git status command
```
$ git diff hello.txt
diff --git a/hello.txt b/hello.txt
index 557db03..980a0d5 100644
--- a/hello.txt
+++ b/hello.txt
@@ -1 +1 @@
-Hello World
+Hello World!
```
### Showing Git Commit Logs

### Committing Your Code

### Git

### Adding Changes to the Staging Area

### Git Project Workflow
