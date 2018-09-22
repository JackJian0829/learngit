Git is a distributed version control system.
Git is free software distributed under the GPL.



git 命令

git add <file>
git commit -m<message>
git status  查看状态
git diff	查看修改内容 或者 git diff HEAD --<file>  比较版本库和工作区中的区别
git reset --hard HEAD^/git reset --hard commit_id
git log  查看提交历史  git log --pretty=oneline
git reflog  查看命令历史
git checkout -- file  丢弃工作区的修改  让这个文件回到最近一次git commit或git add时的状态
git reset HEAD <file> --> git checkout -- file  添加到了暂存区时，想丢弃修改  
git rm <file> 删除一个文件
git checkout 其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。

远程仓库
$ ssh-keygen -t rsa -C "youremail@example.com"   创建SSH Key 生成两个文件 id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥

$ git remote add origin git@github.com:michaelliao/learngit.git  本地仓库和远程版本库关联
$ git push -u origin master    由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。

$ git push origin master  从现在起，只要本地作了提交，就可以通过命令