# Learn Git Branching 
[Interactive Guide](https://learngitbranching.js.org/)

[Sandbox](https://learngitbranching.js.org/?NODEMO)

## Main 

### commit 

Commit usually means a set of changes in practical working, which can be seen as a new version of the current project. 

### branch 

Start a branch, which means including the current commit and its parent commits. Using the command `git checkout branch_name` to switch to different branches. 

### rebase

Changing the base (namely its parent commit) of the current branch. Suppose we have two branches, `main` and `bugFix` with the latest commit `Here is main` and `Fix a bug` respectively. Now we are in a branch `bugFix`, through run command `git rebase main`, we can merge two branches to a new, sequential branch, and now commit `Here is main` is become the parent of `Fix a bug`. And then we can run `git checkout main` to switch branch `main` and `git rebase bugFix` to continue our work. 

## Remote

## Troubleshooting 
[Turn to solutions](https://github.com/YILIN1031/TheMissingSemester/blob/main/git/git.md#troubleshooting)
