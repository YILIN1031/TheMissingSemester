# Learn Git Branching 
[Interactive Guide](https://learngitbranching.js.org/)

[Sandbox](https://learngitbranching.js.org/?NODEMO)

## Main 

### commit 

Commit usually means a set of changes in practical working, which can be seen as a new version of the current project. 

### branch 

Start a branch, which means including the current commit and its parent commits. Using the command `git checkout branch_name` to switch to different branches for your work. 

### rebase

Changing the base from one commit to another one for the current branch. Suppose we have two branches, `main` and `bugFix` with the latest commit `Here is main` and `Fix a bug` respectively. Now we switch to the branch `bugFix`, through run command `git rebase main`, we can merge two branches to a new, sequential branch, and now commit `Here is main` is become the parent of `Fix a bug`. Next, we run `git checkout main; git rebase bugFix` to go to the branch `main` and continue our work. 

### About HEAD
HEAD is the symbolic name for the currently checked out commit. And HEAD always points to the most recent commit which is reflected in the working tree.

**Detaching HEAD:**

Using `checkout` to attach the HEAD to a commit instead of a branch (HEAD points the branches in a default situation).

**About `~`:**

`git branch -f main HEAD~3` means moving (by force) the main branch to three parents behind HEAD.

### Reversing Changes 

`git reset` or `git revert`. `reset` usually use in private branches while `revert` is used in public ones.

### Differences between `branch -f` and `reset`/`revert`

`git branch -f` allows you to move any (local) branch anywhere

`git reset` moves your active branch (HEAD) to the specified commit.

### Modifying the source tree

For modifying the source tree in working, `cherry-pick` and `rebase -i` are useful. 

**Usage:**
~~~
git cherry-pick C5 C3 C4
git rebase -i HEAD~3
~~~

### Making the slight modification

`git commit --amend`

### Using tags 

`git tag tag_name your_commit`

### See the description of a commit 

`git describe your_commit`

Without adding arguments, git will show HEAD default. 

## Remote

## Troubleshooting 
[Turn to solutions](https://github.com/YILIN1031/TheMissingSemester/blob/main/git/git.md#troubleshooting)
