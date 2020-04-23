完成配置：
git config --global user.name "abbiezhu"
git config --global user.email "abbiezhu@gmail.com"

把文件加到git 库
git add 文件名
git commit -m '写信息'

git status 查看状态
git diff 查看修改内容

git log 查 看各个LOG 版本信息
git log --pretty=oneline 单行查看。

git reset --hard HEAD^ 恢复到上一个版本。
git reset --hard HEAD^^ 恢复到上上一个版本。
git reset --hard "commit_ID"

git relog
git reflog 查看版本记录。

git checkout --文件名    撤销修改 （丢弃工作区的修改）。
git checkout -- file 命令中的--很重要，没有--，就变成了“切换到另一个分支”的命令

git reset HEAD <file>可以把暂存区的修改撤销掉

git rm --file  删除版本库的文件
git checkout --file 其实是用版本库里的版本替换工作区的版本，无论工作区是修改还是删除，都可以“一键还原”。


添加SSH KEY..
创建SSH Key。在用户主目录下，看看有没有.ssh目录，如果有，再看看这个目录下有没有id_rsa和id_rsa.pub这两个文件，如果已经有了，可直接跳到下一步。如果没有，打开Shell（Windows下打开Git Bash），创建SSH Key：
ssh-keygen -t rsa -C "abbiezhu@gmail.com"


git remote add origin git@github.com:abbiezhu/wordpress_abbbt4.git
链接到GITHUB 

git push -u origin master
推送到 远程库上。

把本地库的内容推送到远程，用git push命令，实际上是把当前分支master推送到远程。
由于远程库是空的，我们第一次推送master分支时，加上了-u参数，Git不但会把本地的master分支内容推送的远程新的master分支，还会把本地的master分支和远程的master分支关联起来，在以后的推送或者拉取时就可以简化命令。