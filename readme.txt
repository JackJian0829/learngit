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
