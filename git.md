# Git 

## References

[Git documentation](https://git-scm.com/doc)

## Start

[Interactive Guide](https://learngitbranching.js.org/)

[About Git](https://docs.github.com/en/get-started/using-git/about-git#example-contribute-to-an-existing-repository)

[Git Cheat Sheets(PDF)](https://training.github.com/downloads/github-git-cheat-sheet.pdf)

## Some examples from Github docs

[Contribute to an existing repository](https://docs.github.com/en/get-started/using-git/about-git#example-contribute-to-an-existing-repository)

[Start a new repository and publish it to GitHub](https://docs.github.com/en/get-started/using-git/about-git#example-start-a-new-repository-and-publish-it-to-github)

[Contribute to an existing branch on GitHub](https://docs.github.com/en/get-started/using-git/about-git#example-contribute-to-an-existing-branch-on-github)

## Teamwork

[Contributing to projects](https://docs.github.com/en/get-started/quickstart/contributing-to-projects)

## Solution

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