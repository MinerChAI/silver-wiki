# `git`
![](git.png)

This module displays information about the current git repository. If you are not in a git repository, it is not shown. If the current branch is dirty, the segment is yellow/orange (depending on your terminal color scheme).

| Icon                        | Description                                                       |
| :-------------------------: | ----------------------------------------------------------------- |
| ![github](github.png)       | remote points to [GitHub](https://github.com/)                    |
| ![gitlab](gitlab.png)       | remote points to [GitLab](https://gitlab.com/)                    |
| ![bitbucket](bitbucket.png) | remote points to [Bitbucket](https://bitbucket.org/)              |
| ![generic](git-generic.png) | remote does not point to any of the above domains                 |
| ![stash](stash.png)         | a stash
| ![ahead](ahead.png)         | you are a commit ahead of upstream
| ![behind](behind.png)       | you are a commit behind upstream (requires a `git fetch`)         |
| ![circle](circle.png)       | the branch has been modified                                      |
| ![plus](plus.png)           | a file has been staged                                            |
