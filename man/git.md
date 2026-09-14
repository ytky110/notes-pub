# Git

## local

全体確認

`git log`  

コミット

`git add .`  
`git commit`  

作業中確認

`git status`  
`git diff`  

## remote

`git remote add <name> <url>`  
e.g.  
`git remote add github git@github.com:ytky110/example.git`  

`$ git remote [-v]`  
`$ git remote show <name>`  

`gh repo create`  
`git push [-u <remote>] [branch]`  

`git clone <url>`  

変更を取り込む

`git pull [--rebase]`  

`--rebase`: リモートの上にローカルを載せ直す

```
git pull          ~= git fetch + git merge
git pull --rebase ~= git fetch + git rebase
```
