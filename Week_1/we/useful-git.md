# Git

`git stash` - save uncommitted and untracked files in memory in order to be able to switch between branches; should see no files need action when `git status`
`git stash apply` - paste the saved files to current branch

`git branch -d branch_name` - only delete local when you have pushed and merged to remote branches
`git branch -D branch_name` - same as --delete --force, delete regardless of its push and merge status

`git checkout -- file_name(s)...` - reverts file back before changes are made to it after last commit
