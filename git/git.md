# Git 

## References

[Git documentation](https://git-scm.com/doc)

## Start

[Interactive Guide](https://learngitbranching.js.org/)

[Git Cheat Sheets](https://training.github.com/downloads/github-git-cheat-sheet.pdf)

[About Git](https://docs.github.com/en/get-started/using-git/about-git)

[Adding locally hosted code to GitHub](https://docs.github.com/en/get-started/importing-your-projects-to-github/importing-source-code-to-github/adding-locally-hosted-code-to-github)

[How to Write a Git Commit Message](https://cbea.ms/git-commit/)

### Teamwork

[Contributing to projects](https://docs.github.com/en/get-started/quickstart/contributing-to-projects)

## Troubleshooting

### Change Submitted Commit

[How to modify](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/creating-and-editing-commits/changing-a-commit-message)

### Can't Push

show messages below or simliar, and need to wait long time for pushing.

~~~
Delta compression using up to 4 threads, git cannot push
~~~

Solution ways:

[Increase the buffer](https://developercommunity.visualstudio.com/t/i-cannot-push/358360)

~~~
git config --global --unset http.postBuffer 524288000
~~~

[Remove the previous commits](https://stackoverflow.com/questions/70968685/git-push-failure)

~~~
git reset --soft HEAD~n
~~~

### Remote origin already exists

~~~
$ git remote add origin https://github.com/octocat/Spoon-Knife.git
> fatal: remote origin already exists.
~~~

Solution:

[Renaming the remote repository](https://docs.github.com/en/get-started/getting-started-with-git/managing-remote-repositories#renaming-a-remote-repository)

~~~
$ git remote -v
# View existing remotes
> origin  https://github.com/OWNER/REPOSITORY.git (fetch)
> origin  https://github.com/OWNER/REPOSITORY.git (push)

$ git remote rename origin destination
# Change remote name from 'origin' to 'destination'

$ git remote -v
# Verify remote's new name
> destination  https://github.com/OWNER/REPOSITORY.git (fetch)
> destination  https://github.com/OWNER/REPOSITORY.git (push)
~~~




