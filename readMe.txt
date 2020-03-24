This project is solely created to explore git


1) For reverting back tha last commit into local 
 git reset HEAD~1
 
2) For completely reverting without even looking at the changes for example in case of production.
git reset --hard HEAD~1

 and then commit and push
https://stackoverflow.com/questions/927358/how-do-i-undo-the-most-recent-local-commits-in-git/34547846

3) Git has one remote and one local brannch.When you checkout it gives you the local branch for example in case of git checkout master , it will be local data only with +- comits ahead .For sync you need to do git pull

4) Resolving git conflict
https://stackoverflow.com/questions/161813/how-to-resolve-merge-conflicts-in-git
