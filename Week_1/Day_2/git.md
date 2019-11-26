# Git

## If you cloned a gist and forgot to use the fork of it, and you want to redirect the changes to the forked gist, then:
`git remote set-url origin <forked gist link>`

## If you forgot to save the file before committing and want to combine the changes to one commit message
1. commit the change with the same message
2. `git rebase -i HEAD~<number of recent commits to change>`
3. in the vim editor change the `pick` to `squash` to have the squashed combined to the pick commit message
