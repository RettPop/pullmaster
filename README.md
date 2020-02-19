# pullmaster
Bash script to rebase local git branch with local master

# Usage
`pullmaster [branch]`
  
  `branch` - optional custom branch name to rebase from. Default: _master_

# Usecase
When you are going to work with several features and have only one git branch (like in case with Gerrit), it is pretty convenient to have set of local development branches to switch between code revisions. Then you have to keep your local master updated and branches rebased on top of it. What the script does is:

1. stores current branch
1. checkout [branch] (passed as a first parameter, *master* by default)
1. makes `git pull`
1. check out back stored branch
1. makes `git rebase [branch]`

Script stops on any error it facing.
