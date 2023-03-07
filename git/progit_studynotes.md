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

## Git Branching 

[Interactive Guide - Learn Git Branching](https://github.com/YILIN1031/TheMissingSemester/blob/main/git/learn_git_branching.md)

## Troubleshooting 
[Turn to solutions](https://github.com/YILIN1031/TheMissingSemester/blob/main/git/git.md#troubleshooting)
