# Pro Git, Study notes
[Book: Pro Git](https://git-scm.com/book/en/v2)

## Git Basics

### Checking the Status of Your Files

`git status`

### Ignoring Files

Often, you’ll have a class of files that you don’t want Git to automatically add or even show you as being untracked. These are generally automatically generated files such as log files or files produced by your build system. In such cases, you can create a file listing patterns to match them named .gitignore.

~~~
# ignore all .a files
*.a

# but do track lib.a, even though you're ignoring .a files above
!lib.a

# only ignore the TODO file in the current directory, not subdir/TODO
/TODO

# ignore all files in any directory named build
build/

# ignore doc/notes.txt, but not doc/server/arch.txt
doc/*.txt

# ignore all .pdf files in the doc/ directory and any of its subdirectories
doc/**/*.pdf
~~~

### Removing and move in staging area

`git rm` & `git mv`

### See the the commit history in graph

Use command `git log --graph` or install the visual extension in VSCode, [here](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph) 

### Preventing the display of merge commits

Depending on the workflow used in your repository, it’s possible that a sizable percentage of the commits in your log history are just merge commits, which typically aren’t very informative. To prevent the display of merge commits cluttering up your log history, simply add the log option `--no-merges`.

### Undoing things

redo the commit:

~~~
$ git commit -m 'Initial commit'
$ git add forgotten_file
$ git commit --amend
~~~
> **NOTE:** 
>
> It’s important to understand that when you’re amending your last commit, you’re not so much fixing it as replacing it entirely with a new, improved commit that
> pushes the old commit out of the way and puts the new commit in its place. 
>
> Only amend commits that are still local and have not been pushed somewhere. Amending previously pushed commits and force pushing the branch will cause problems for > > your collaborators. 

[Git Basics - Undoing Things](https://git-scm.com/book/en/v2/Git-Basics-Undoing-Things)

### Remote introduction

show the remote:

`git remote -v`

adding:

`git remote add <shortname> <url>` and then `git fetch <shortname>` 

pushing: 

If you want to push your master branch to your origin server (again, cloning generally sets up both of those names for you automatically), then you can run this to push any commits you’ve done back up to the server.

`git push origin master`

Inspecting a Remote: 

`git remote show <remote>`

Renaming remotes & remove: 

You can run `git remote rename` to change a remote’s shortname. And `git remote remove` for removing the remotes. 

~~~
$ git remote rename pb paul
$ git remote
origin
paul
~~~

~~~
$ git remote remove paul
$ git remote
origin
~~~

### Tagging

`git tag -h`

## Git Branching 

[Interactive Guide - Learn Git Branching](https://github.com/YILIN1031/TheMissingSemester/blob/main/git/learn_git_branching.md)

## Distributed Git

### Contributing to a Project
> [Reference Link](https://git-scm.com/book/en/v2/Distributed-Git-Contributing-to-a-Project)

Private Small Team (two people collaboration):

![General sequence of events for a simple multiple-developer Git workflow](https://git-scm.com/book/en/v2/images/small-team-flow.png)

Private Managed Team:

![Private Managed Team](https://git-scm.com/book/en/v2/images/managed-team-flow.png)

### Maintaining a Project 

### ...

...

## Troubleshooting 
[Turn to solutions](https://github.com/YILIN1031/TheMissingSemester/blob/main/git/git.md#troubleshooting)
