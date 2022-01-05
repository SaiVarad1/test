# Git Practice

Tutorial Link: https://www.youtube.com/watch?v=DVRQoVRzMIY

* Use `git init` to be able to track files 
* using multiple branches: `git checkout -b **branchname**`

## Remote Repo Stuff:
    * Make a repo on GitHub
    * make sure you are on master branch
    * copy the line 
    git remote add origin https://github.com /SaiVarad1/test.git

    * push to remote by using git push -u origin master
    ** This tells it to push all commits to the remote branch Master)
    (-u saves settings so you can just use git push next time)


* Making this change in the Remote Repo

## Reverting to previous commit:

* git revert address 
    * NOTE: revert only reverses changes of specified commit

**NOTE: CAN REPLACE HEAD^(which means commit before Head) WITH ANY COMMIT ADDRESS**
* git reset --hard HEAD^
    * And if you actually want to completely undo it, throwing away all uncommitted changes, resetting everything to the previous commit 
* **git reset --soft HEAD^**
    * undos act of commiting, but leaves previous files staged
* git reset HEAD^
    * If you want to undo the act of committing and everything you'd staged, but leave the work tree (your files) intact (undos both commit and staging)

* Source: https://stackoverflow.com/questions/2845731/how-to-uncommit-my-last-commit-in-git
* `git log --oneline` to view entire log

## Git Diff command
https://www.techiedelight.com/find-differences-between-two-commits-git/

* `git diff <commit-id><commit-id>`
* `git diff HEAD^ HEAD` or `git diff HEAD^..HEAD`
    * Lists out all changes since last commit 
    * `git diff HEAD^..`
* specified file comparison
    * `git diff HEAD^ HEAD -./file`
* ## Listing out names of changed files
  
    * ### `git diff HEAD~5..HEAD --name-status`
        * `HEAD~5` refers to the last 5 commits
    * ### `git diff HEAD~5 HEAD --stat` or  `git diff HEAD~5 HEAD --compact-summary`
    * ### To view changes between last commit and uncommitted edits: 
        * ###    `git diff HEAD^ --stat`



## Git errors encountered and Solutions:
* Another git process seems to be running in this repository, e.g.
are terminated then try again. If it still fails, a git process
may have crashed in this repository earlier:
remove the file manually to continue.

        Solution: rm -f .git/index.lock


## Branching
* To delete a file on only one branch, commit afterwards
* To save edits after switching to a previous commit, create a new branch using `git switch -c branchName`
    ### Merging
        * to merge specific files from a branch, use git checkout branchName path

