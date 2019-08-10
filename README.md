# Basic Git Commands
Git is the free and open source distributed version control system that's responsible for everything GitHub
related that happens locally on your computer. This refers the most important and commonly
used Git commands for easy reference.
> You can download the pdf format from [here](https://drive.google.com/open?id=1H9h8UCDP2KIXedLFC1lJQqJIQuoTBLWg).

---
## Sections
* [Git Basics](#git-basics)
* [Remote Repository](#git-remote-repository)
* [Branching And Merging](#branching-and-merging)
* [Git Config](#git-config)
* [Git Log](#git-log)
* [Rewriting History](#rewriting-history)
* [Undoing Changes](#undoing-changes)





---
## Git Basics
|Commands                 | Usage       |
|:---                     |:---         |
|  `git init`                       |Creates a git repository in specified Directory.  |
| `git init --bare`                 |Bare Repository that contains no project data, only *.git* folder data. |
|`git clone <url>`                  |To clone existing directory into the workspace.|
|`git config user.name <name>`     |Defines the author name to be used by all commits in current repository. __--global__ flag is used for current user.|
|`git add <directory>`             |Stage all changes in _\<directory>_ *or* _\<file>_ *or* __.__ for all files in workspace.|
|`git commit -m <message>`         |Commit the staged snapshot with _\<message>_ |
|`git commit -am <message>`        |Add and commit tracked file changes with _\<message>_ |
|`git status`                      |List which file is staged, unstaged or untracked.|
|`git log`                         |Display entire commit history using default format.|
|`git diff`                        |Shows unstaged changes between your _Index_ and working directory.|
---

## Git Remote Repository

|Command                            |Usage|
|:---                               |:--- |
|`git remote add <name> <url>`      | Creates a new connection to a remote repository. You can use _\<name>_ as  shortcut  for _\<url>_ <br/> in other commands. __Example__ : `git remote add origin master`|
|`git remote rm <name>`             |Remove a remote connection|
|`git remote -v`                    |Display all the remotes _\<name>_ with _\<url>_.|
|`git fetch <remote> <branch>`      | Fetch the specified _\<branch>_ from _\<remote>_. `git fetch <remote>` <br/>to fetch all _branches_.
|`git pull <remote>`                | Fetch the current branch and immediately merge into the local branch.|
|`git pull <remote> <branch>`       |Fetch the specified _\<branch>_ and merge it into the local copy.
|`git push <remote> <branch>`       |Push the _\<branch>_ to _\<remote>_ with necessary commits and object.<br/>Create a named branch in the branch remote repo if it doesn't exit.|
|`git push <remote> --delete <branch>`| Deletes a _\<remote>_ _\<branch>_.|
|`git push <remote> <branch> --force` | Push the _\<branch>_ forcefully and update the _remote/branch_.
---

## Branching and Merging
|Command            |Usage              |
|:---               |:---               |
|`git branch`                       | List all local branches.|
|`git branch -a`                    | List all branches local and remote.|
|`git branch <branchName>`          | Create a new Branch|
|`git branch -d <branchName>`       | Delete a local branch. __-D__ for hard delete.|
|`git branch <remote> --delete <branchName>`|Delete a remote branch.|
|`git checkout -b <branchName>`      |Create a new branch _\<branchName>_ and switch to it.|
|`git checkout -b <branchName> <origin/branchName>` | Clone a new branch and switch to it.|
|`git branch -m <oldBranchName> <newBranchName>`    | Rename a local branch.|
|`git checkout <branchName>` | Switch to _\<branchName>_.
|`git checkout --<fileName>`        | Discard changes to a file.|
|`git merge <branchName>`           | Merge a branch into active branch.|
|`git merge <source> <target>`      | Merge _\<sourceBranch>_ to _\<targetBranch>_.
|`git stash`                        | Stash changes in working directory.|
|`git stash clear`                  | Remove all stashed entries.|
---

## Git Config
|Command                     |Usage        |
|:---                        |:---         |
|`git config --global user.name <name>`| Define the author name to be used for all commits by current user.|
|`git config --global user.email <email>`|Define the author email to be used for all the commits by current user.|
|`git config --system core.editor <editor>`| Set the text editor.|
|`git config --global --edit`             |Open  global config file in a text editor.|
|`git config --global alias.<aliasName> <command>`  | Create a shortcut for git command.| 

---
## Git Log
|Command                    |Usage         |
|:---                       |:---          |
|`git log -limit`           | Limit number of commits. **Example** : `git log -5`|
|`git log --oneline`        |Condense each commit to single line.|
|`git log -p`               |Display the full difference of each commit.|
|`git log --stat`           |Includes which file were altered and the relative number of lines.|
|`git log --author="<pattern>"`  |Search for commits by a particular author.|
|`git log --grep="<pattern>"`    |Search for commits with a commit message that matches a _pattern_.|
|`git log <since> ... <until>`      | Shows commits that occur between two commits, branch Name, HEAD or any kind of reference.|
|`git log --<fileName>`             |Only display commits that have specified file.|
|`git log --graph --decorate`       |Display a text based graph of commits on left side of commit|
|`git log before= "<Date>" --pretty=format :"%c"` | shows log of commit before specified commit date.| 
|`git log after= "<Date>" --pretty=format :"%c"` | shows log of commit after specified commit date.|  
|`git log --after "Date" --before "Date"`|Filter commits by date range.|
|`git log --pretty=format:<options>`| Print log in specified format.

---
### Format table
|Format     |Defination|
|:---       |:---      |
|`%H`       | Commit hash|
|`%h`       | Abbreviated Commit hash|
|`%T`       | Tree hash|
|`%t`       | Abbreviated tree hash|
|`%an`      | Author name|
|`%as`      | Author email|
|`%cd`      | Committer Date|
|`%s`       | Commit message|

---
## Rewriting History
|Command        |Usage          |
|:---           |:---           |
|`git commit --amend`|Replace the last commit staged changes and last commit combined using with nothing staged to edit commit message.|
|`git rebase <base>`|Rebase current branch to _tag_, _commit_ or _reference_.|
|`git reflog`|shows a log of changes to local repository's HEAD.|

----

## Undoing changes
|Command|Usage|
|:---|:---|
|`git revert <commit>`|Create a new commit that undergoes all the changes made in _\<commit>_ then apply it to current branch.|
|`git reset <file>`|Removes the file from staging area, but leaves the working directory unchanged.|
|`git clean -n`|Show which files would be removed from working directory.|
|`git clean -f`|Cleans the files from working directory.|














