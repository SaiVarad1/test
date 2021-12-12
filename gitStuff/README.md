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



    * Making this change in the local Repo (conflicting change made locally without pulling first)

* Making this change in the Remote Repo

* CONFLICTING CHANGE 1 

## Reverting to previous commit:
* git revert --no-commit 02119cdbdb4db640fc51ab0681bdafbc3bcd7756..HEAD
* or just git revert address 

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
