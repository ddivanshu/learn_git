This project is solely created to explore git


1) For reverting back tha last commit into local 
 git reset HEAD~1
 
2) For completely reverting without even looking at the changes for example in case of production.
git reset --hard HEAD~1
 and then commit and push
https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git/34547846

3) Git has one remote and one local brannch.When you checkout it gives you the local branch for example in case of git checkout master , it will be local data only with +- comits ahead .For sync you need to do git pull

4) How to merge previous commits into single commit

5)How to change message of previous commit

4) Scenario : Reverting last merge / last comit in the branch like when production system fails.
   Command : git revert HEAD , then git push
   This wont override anything but will create a new commit over latest commit nullfyling its affect.
   
  6)When remote branch is ahead of curent branch. 
  git pull
  (resolve conflicts)
  git merge --continue
  repeat
  git push
  
  7) Resolving merge conflict using merge
  
  8)Resolving merge conflict using rebase
  
  9)When to use merge and when rebase?

10)Remove file after it has been pushed.

