# Merge
https://www.atlassian.com/git/tutorials/using-branches/git-merge
## Start a new feature
git checkout -b new-feature main
## Edit some files
git add <file>
git commit -m "Start a feature"
## Edit some files
git add <file>
git commit -m "Finish a feature"
## Merge in the new-feature branch
git checkout main
git merge new-feature
git branch -d new-feature
  
# Fast Forward Merge
  git merge --no-ff <branch>
  
#3-way merge

  Start a new feature
git checkout -b new-feature main
## Edit some files
git add <file>
git commit -m "Start a feature"
## Edit some files
git add <file>
git commit -m "Finish a feature"
## Develop the main branch
git checkout main
## Edit some files
git add <file>
git commit -m "Make some super-stable changes to main"
## Merge in the new-feature branch
git merge new-feature
git branch -d new-feature
  
# Rebase
  Rebasing is the process of moving or combining a sequence of commits to a new base commit. 
 
## Create a feature branch based off of main
  https://www.atlassian.com/git/tutorials/rewriting-history/git-rebase
git checkout -b feature_branch main
## Edit files 
git commit -a -m "Adds new feature" 
## Git rebase in standard mode will automatically take the commits in your current working branch and apply them to the head of the passed branch.
  git rebase <base>
## Interactive 
  git rebase --interactive <base>
## Advanced Rebase
  git rebase --onto <newbase> <oldbase>
