# Learn Git Branching 
[Interactive Guide](https://learngitbranching.js.org/)

[Sandbox](https://learngitbranching.js.org/?NODEMO)

## Main 

### commit 

Commit usually means a set of changes in practical working, which can be seen as a new version of the current project. 

### branch 

Start a branch, which means including the current commit and its parent commits. Using the command `git checkout branch_name` to switch to different branches for your work. 

### rebase

Changing the base from one commit to another one for the current branch. Suppose we have two branches, `main` and `bugFix` with the latest commit `Here is main` and `Fix a bug` respectively. Now we switch to the branch `bugFix`, through run command `git rebase main`, we can merge two branches to a new, sequential branch, and now commit `Here is main` is become the parent of `Fix a bug`. Next we run `git checkout main; git rebase bugFix` to go the branch `main` and continue our work. 

### About HEAD
HEAD can be seen as a pointer, It can point to both commits and branches. 

**Detaching HEAD:**

Using `checkout` to attach the HEAD to a commit instead of a branch (HEAD points the branches in a default situation).

**About `~`:**

`git branch -f main HEAD~3` means moving (by force) the main branch to three parents behind HEAD.

### Reversing Changes 

`git reset` or `git revert`. `reset` usually use in private branches while `revert` is used in public ones.

## Remote

## Troubleshooting 
[Turn to solutions](https://github.com/YILIN1031/TheMissingSemester/blob/main/git/git.md#troubleshooting)
