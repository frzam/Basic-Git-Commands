# Basic Git Commands

## Sections
* [Git Basics](#git-basics)










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
|`git remote add <name> <url>`      | Creates a new connection to a remote repository. You can use _\<name>_ as shortcut for _\<url>_ in other commands. __Example__ : `git remote add origin master`|
|`git remote rm <name>`             |Remove a remote connection|
|`git remote -v`                    |Display all the remote _\<name>_ with _\<url>_.