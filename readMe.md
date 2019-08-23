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






