# Learn Git Branching 
[Interactive Guide](https://learngitbranching.js.org/)

[Sandbox](https://learngitbranching.js.org/?NODEMO)

## Main 

### commit 

Commit usually means a set of changes in practical working, which can be seen as a new version of the current project. 

### branch 

Start a branch, which means including the current commit and its parent commits. Using the command `git checkout branch_name` to switch to different branches for your work. 

Create a new branch and switch to it:

`git checkout -b <newbranchname>`

Changing a branch name:
> [Git Branching - Branch Management](https://git-scm.com/book/en/v2/Git-Branching-Branch-Management)

`git branch --move bad-branch-name corrected-branch-name`

This replaces your `bad-branch-name` with `corrected-branch-name`, but this change is only local for now. To let others see the corrected branch on the remote, push it using: 

`git push --set-upstream origin corrected-branch-name`

After you’ve done all these tasks, and are certain the main branch performs just as the master branch, you can delete the master branch:

`$ git push origin --delete bad-branch-name`

### rebase

Changing the base from one commit to another one for the current branch.  
> Rebase local changes before pushing to clean up your work, but never rebase anything that you’ve pushed somewhere.

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

`git describe your_commit`, It is necessary to creat a `tag` for a commit before run `describe`. 

Without adding arguments, git will show HEAD default. 

## Remote

### Git Remote Branches

Remote branches are on your local repository, not on the remote repository.

`git remote show <remote>` 

### What is `origin/`

if a branch named `origin/main` (**`<remote name>/<branch name>`**), the branch name is `main` and the name of the remote is `origin`.

### `git fetch`

`git fetch` performs two main steps, and two main steps only.

* downloads the commits that the remote has but are missing from our local repository
* updates where remote branches point (for instance, origin/main)

### Specify remote head. Push. Delete. 

`git remote set-head origin other_remote_branch` 

`git push origin HEAD:other_remote_branch` 

`git branch -d -r origin/other_remote_branch` 

### See the tracking branches

If you want to see what tracking branches you have set up, you can use the -vv option to git branch. This will list out your local branches with more information including what each branch is tracking and if your local branch is ahead, behind or both.

~~~
$ git branch -vv
  iss53     7e424c3 [origin/iss53: ahead 2] Add forgotten brackets
  master    1ae2a45 [origin/master] Deploy index fix
* serverfix f8674d9 [teamone/server-fix-good: ahead 3, behind 1] This should do it
  testing   5ea463a Try something new
~~~

### A separate development branch 

1. Create a new branch `dev` from `main` in Github, and do `git pull`, `git branch -a` to confirm the new remote branch is in your local repository. 
2. `git checkout -b dev origin/dev` to create the development branch. (Or `git branch -u origin/dev dev`)
3. Begin working...
4. `git add .` & `git commit -m "..."` 
5. Push your work from local dev to remote dev: `git push` 
7. Merge your work to `origin/main`. 

   Firstly, `git pull origin main`, make sure everything is the newest. Next, `git checkout main` and `git merge origin/dev`. Finally, `git push origin main`.
   
   (Or you can merge in Github directly)
   
> **[Turn to Teamwork](https://github.com/YILIN1031/TheMissingSemester/blob/main/git/git.md#teamwork)**

## Troubleshooting 
[Turn to solutions](https://github.com/YILIN1031/TheMissingSemester/blob/main/git/git.md#troubleshooting)
