# Basic Git Commands

## Sections
* [Git Basics](#git-basics)
* [Remote Repository](#git-remote-repository)









## Git Basics

---
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


## Git Remote Repository
---
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

## Git config
---
|Command                     |Usage        |
|:---                        |:---         |
|`git config --global user.name <name>`| Define the author name to be used for all commits by current user.|
|`git config --global user.email <email>`|Define the author email to be used for all the commits by current user.|
|`git config --system core.editor <editor>`| Set the text editor.|
|`git config --global --edit`             |Open  global config file in a text editor.|
|`git config --global alias.<aliasName> <command>`  | Create a shortcut for git command.| 






















