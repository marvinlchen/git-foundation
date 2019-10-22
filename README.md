
### 一、新建分支
#### 1） clone远程仓库
git clone 服务器地址
#### 2）新建+切换分支
git checkout -b hotfix
等于 git branch hotfix + git checkout hotfix
#### 3）切换分支
git checkout hotfix
#### 4）推送指定分支（不追踪）
git push origin hotfix
#### 5）推送当前分支并追踪
git push --set-upstream origin HEAD
#### 6）查看本地分支和远程分支关系 
git branch       （本地分支）
git branch -vv   （带关系）
git branch -a    （带远程分支）
### 二、跟踪已有远程分支(4种方法，任选其一)
#### 1）git checkout -b branch-name origin/develop
在远程分支的基础上建立分支，并且追踪origin/branch-name远程分支。
#### 2) git branch --set-upstream branch-name origin/branch-name
将branch-name分支追踪远程分支origin/branch-name
#### 3）git branch -u origin/branch-name
将当前分支跟踪远程分支origin/branch-name
#### 4）git clone -b branch-name 服务器地址
自动将创建好的branch-name分支追踪origin/branch-name分支
### 三、提交代码
#### 1）查看是否本地有修改
git diff
git status -s 
#### 2）添加到Staged
git add .
查看添加 git diff --staged
#### 3）提交内容
git commit
查看提交 git show
#### 4）push提交
git push
查看push结果  git show HEAD
#### 5）rebase提交
git rebase -i master
git checkout master
git push
### 四、同步代码
#### 1）拉取到本地仓库
git fetch 
等于 git fetch origin branch-name
#### 2) 对比分支修改
git diff HEAD FETCH_HEAD
git diff HEAD origin/branch-name
#### 3）合并代码
git merge
等于 git merge origin/branch-name
#### 4）拉取+合并
git pull
等于 git fetch origin branch-name + git merge origin/branch-name
#### 5) IDE冲突解决
vscode
五、删除分支
#### 1）删除远端分支
git push origin :branch-name
#### 2）删除本地分支
git branch -d hotfix
六、其他
#### 1）查看提交日志
git log --oneline --decorate --graph —all
可视化 Sourcetree
#### 2）暂存当前修改
git stash
git stash list
git stash pop
