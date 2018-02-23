# pullmaster
Bash script to rebase local git branch with local master

# Usecase
When you are going to work with several features and have only one git branch (like in case with Gerrit), it is pretty convenient to have set of local development branches to switch between code revisions. Then you have to keep your local master updated and branches rebased on top of it. What the script does is:

1. stores current branch
1. checkout <main branch> (passed as a first parameter, *master* by default)
1. makes _git pull_
1. check out back development branch
1. makes _git rebase <main branch>_

Script stops on any error it facing. 
