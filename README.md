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
#### Example git diff command
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
In Git, the git log command shows all of the commit logs for a project. The following is displayed for each commit:
<ul><li>A 40-character code, called a SHA, that uniquely identifies the commit.
 <ul></ul><li>The commit author
  <ul></ul><li>The date and time of the commit
    <ul></ul><li>The commit message
 
</ul> This command is particularly useful when you need to refer back to an old version of your project. The unique SHA code allows you to identify a point in your program’s history that you would like to revert to.

#### Example git Logs command
```
$ git log
commit 9d63f80111447544c303e9f1776fa08593a87310
Author: user1 <exampleuser@email.com>
Date:   Wed Jan 13 18:55:53 2021 +0000
 
    Added updates to the file
 
commit 3ba6efbeece6ed530d85de5e313e52123fdf8cb4
Author: user1 <exampleuser@email.com>
Date:   Wed Jan 6 10:11:13 2021 -0400
 
    Completed first line of dialogue
    
  ```

### Committing Your Code
The git commit -m "log message here" command creates a new commit containing:
<ul><li>The current contents of the staging area
 <ul></ul><li>A log message describing the changes to the repository
 
 #### Example git Logs command
```
$ git commit -m "Added About section to README"
[master 9d63f80] Added About section to README
1 file changed, 10 insertions(+), 1 deletion(-)
```
A commit is the last step in our Git workflow. A commit permanently stores changes from the staging area inside the repository. This command is almost always used in conjunction with the git add command as git add is used to add files to the staging area.

### Git
Git is a command line software that keeps track of changes made to a project over time. Git works by recording the changes made to a project, storing those changes, then allowing a programmer to reference them as needed.
All Git commands follow the pattern git <action> and, in order to use Git for a project, a project must first be initialized using the git init command in the project’s root directory.
 
### Adding Changes to the Staging Area
The **git add filename** command is used to add the filename file to the staging area. After your changes have been staged, you can use the git commit command to permanently store your changes.
 #### Example git add command
```
$ git add file.text
$ git status
On branch master

Initial commit

Changes to be commited:
  use ("git rm --cached <file> ..." to unstage)
  
         new file: file.text
```

### Git Project Workflow
A Git project has three parts:
<ul><li>A Working Directory: where files are created, edited, deleted, and organize
 <ul></ul><li>A Staging Area: where changes that are made to the working directory are listed
 <ul></ul><li>A Repository: where Git permanently stores changes as different versions of the project
 
 </ul> The Git workflow consists of editing files in the working directory, adding files to the staging area, and saving changes to a Git repository.
 
 ### Git SETUP
 Configuring user information used across all local repositories
 ```
 git config --global user.name “[firstname lastname]”
 ```
 set a name that is identifiable for credit when review version history
 
 ```
 git config --global user.email “[valid-email]”
 ```
 set an email address that will be associated with each history marker
 
 ```
 git config --global color.ui auto
 ```
 set automatic command line coloring for Git for easy reviewing
