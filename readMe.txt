Github

1) For reverting back tha last commit into local 
 git reset HEAD~1
 
2) For completely reverting without even looking at the changes for example in case of production.
git reset --hard HEAD~1
 and then commit and push
https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git/34547846

3) Git has one remote and one local brannch.When you checkout it gives you the local branch for example in case of git checkout master , it will be local data only with +- comits ahead .For sync you need to do git pull

4) How to merge previous commits into single commit : use interactive rebase and squash or fixup

5)How to change message of previous commits.Use ineractive rebase and use reword.

6)Change previous commit:
git commit --amend -m "abccc"
you can add more file and all the staged filed will adup in previous commit with new message.

7) Scenario : Reverting last merge / last comit in the branch like when production system fails.
   Command : git revert HEAD , then git push
   This wont override anything but will create a new commit over latest commit nullfyling its affect.
  
6)When remote branch is ahead of curent branch. 
  git pull
  (resolve conflicts)
  git merge --continue
  repeat
  git push
  
8) Resolving merge conflict using merge
  checkout feature branch
  git pull origin master
  resolve conflicts and add file to staging
  git merge --continue
  Repeat
  git push
  
  
9)Resolving merge conflict using rebase
 go to feature branch
 git rebase master
 resolve conflict
  git rebase --continue
repeat
git push
 
  
10)When to use merge and when rebase?

11)Remove file after it has been pushed.

12) interactive rebase
git rebase -i HEAD~3

13) cherry pick : Picking up commit from some other branch and applying changes on current branch.
git cherry-pick commitHash or git cherry-pick --no-commit commitHash 
( In the former commit will be made and in later it would be added in staging) 
https://www.atlassian.com/git/tutorials/cherry-pick
 

14) git bisect

12) interactive rebase
git rebase -i HEAD~3

13) cherry pick : Picking up commit from some other branch and applying changes on current branch.
git cherry-pick commitHash or git cherry-pick --no-commit commitHash 
( In the former commit will be made and in later it would be added in staging) 
https://www.atlassian.com/git/tutorials/cherry-pick
 

14) git bisect will help youin finding bug using binary search .
git bisect start
git bisect good commithash
git bisect bad commithash
git bisect good
git bisect bad


15)Git show will tell you exact author details, commit message and what changes to which file were done.
example git show commithash

16)git reset hard soft mixed
https://stackoverflow.com/questions/3528245/whats-the-difference-between-git-reset-mixed-soft-and-hard
When using git reset --soft HEAD~1 you will remove the last commit from the current branch, but the file changes will stay in your working tree. Also the changes will stay on your index, so following with a git commit will create a commit with the exact same changes as the commit you "removed" before.
