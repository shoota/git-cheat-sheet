git-cheat-sheet
===============

my git command cheat sheet


### branch操作系

#### 特定ブランチの特定のcommitだけmergeしたい


```
# masterにmergeする場合
$ git checkout master
$ git cherry-pick commit_id(SHA)
$ git push origin master
```
