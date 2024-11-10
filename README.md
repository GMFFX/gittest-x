# gittest-x

暂存文件 -add

* git add  [filename]
* git add .
* add 相当于放入更改的文件进入缓存，可等待多次修改一次更新

commit 将所有缓存内容都提交至分支（本地某分支）

* git commit -m "meaasge"
* git commit --amend -m "message"    如果上次提交暂存的`messge`写错了可以使用使用命令来更新提交，而不需要撤销并重新提交
*

切换到某分支(已存在分支)：git checkout develop  (不建议使用)

* 在 Git 2.23 版本之前，`git checkout` 被广泛用于切换分支和恢复文件。但为了减少混淆，Git 引入了两个新的命令： `git switch [branch_name]`：用于切换分支。`git restore`：用于恢复文件

创建新分支并切换到新分支：git checkout -b develop

* 删除分支 git branch -d  [branch_name]
* `需要注意，在删除分支之前，要先切换到其他分支，否则就会报错。`
* `分支可能有未提交的代码，有时 Git 会拒绝删除本地分支强制删除本地分支git branch -D [branch_name]`

如果存在git子模块，即嵌套文件夹存在自己的 `.git` 目录和版本控制系统，不能直接在父仓库中修改它的文件，需要切换到子模块目录中进行修改和提交。
