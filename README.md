git-cheat-sheet
===============

my git command cheat sheet


### remote/local同期系

#### 強制的にremoteで上書き

```
$ git fetch origin
$ git reset --hard origin/master
```

#### remoteのpushを取り消す

```
$ git pull origin master
$ git reset --hard HEAD^
$ git push -f origin HEAD^:master
```

#### remoteにpushしたか忘れた

```
# master branch の場合
$ git log origin/master..master
```

#### forkしたリポジトリの変更を取り入れる

```
$ git remote add upstream <forked_repo_uri> ## add remote 
$ git fetch upstream
$ git merge upstream/master ## cherry-pickでもいいかも
```

### branch操作系

#### 特定ブランチの特定のcommitだけmergeしたい


```
# masterにmergeする場合
$ git checkout master
$ git cherry-pick commit_id(SHA)
$ git push origin master
```
