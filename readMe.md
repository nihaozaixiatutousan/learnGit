# git
prefers
----

## demo:

git init 初始化项目文件; 

git add newfile 文件添加到git仓库

git  commit -m 'new message'  git仓库中的文件提交到git-->master分支中

## git 版本管理

+ 版本回退
  
  - git log  查看版本提交记录

  - git log --pretty=online  简化版查看版本提交记录

  -  git reset --hard HEAD^  回退上一次提交版本

  -  git reflog  查看每一次命令（可从中找出你误删除的版本)


  -   git reset --hard e375afc(此为版本号头） 回退到你想回退的版本号


git diff HAED -- filename 查看工作区与版本库中文件的不同 



## 撤销修改

git checkout --  filename  可以把未提交的工作区文件撤销
注：没有 -- 的话就会变成切换另一分支

git reset HEAD <file> 可以把提交到暂存区的修改撤销重新放回工作区；

## 远程仓库

ssh-keygen -t rsa -C '283421724@qq.com'  创建ssh key

git remote add origin git@github.com:nihaozaixiatutousan/learnGit.git 此方法可以仓库的名字简写为 origin

```
    git push -u origin master   把本地master分支推送到远程仓库。

    注： -u  git不仅会把master分支推送 其他分支也会被推送。 

```
git clone <ssh || https>  可以把远程仓库克隆到本地


## 分支管理

git branch <name>  创建分支名字

git checkout <name>  切换到name分支

git checkout -b <name> 创建name分支并切换到name分支

git branch 查看所拥有的的分支

git branch -d dev 删除dev 分支
<<<<<<< HEAD
=======

git log --graph 可查看分支合并情况

git merge --no-ff -m 'close fast forward' dev  表示禁用fast forward可以更直观的观察合并情况

git stash 存储分支工作情况，工作情况，不想提交修改的时候

git stash list 查看隐藏内容编号

git stash apply 恢复内容但不删除

git stash drop  删除隐藏区中的内容

git stash pop  恢复并删除

git stash apply  stash@{0}  通过隐藏区中给定的编号指定恢复

git cherry-pick <number&string> 恢复指定的提交到当前分支
>>>>>>> 0e1bdb3... git stash command annotaton
