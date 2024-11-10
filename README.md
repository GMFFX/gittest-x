# gittest-x

暂存文件 -add

* git add  [filename]
* git add .
* add 相当于放入更改的文件进入缓存，可等待多次修改一次更新

commit 将所有缓存内容都提交至分支（本地某分支）

* git commit -m "meaasge"
* git commit --amend -m "message"    如果上次提交暂存的`messge`写错了可以使用使用命令来更新提交，而不需要撤销并重新提交

切换到某分支(已存在分支)：git checkout develop  (不建议使用)

* 在 Git 2.23 版本之前，`git checkout` 被广泛用于切换分支和恢复文件。但为了减少混淆，Git 引入了两个新的命令： `git switch [branch_name]`：用于切换分支。`git restore`：用于恢复文件

创建新分支并切换到新分支：git checkout -b develop

* 删除分支 git branch -d  [branch_name]
* `需要注意，在删除分支之前，要先切换到其他分支，否则就会报错。`
* `分支可能有未提交的代码，有时 Git 会拒绝删除本地分支强制删除本地分支git branch -D [branch_name]`

如果存在git子模块，即嵌套文件夹存在自己的 `.git` 目录和版本控制系统，不能直接在父仓库中修改它的文件，需要切换到子模块目录中进行修改和提交。


推送分支

* 法1  `git push -u origin <branch_name>`

  * `<branch_name>`是本地分支的名称
  * 命令会将本地分支推送到远程仓库`origin`下的同名分支（不存在则自动创建）并设置关联。`-u`（或`--set - upstream`）选项的作用是同时设置本地分支和远程分支的关联，这样以后执行`git push`或`git pull`时，Git 就知道对应的远程分支了。
* 法2推送且创建：  `git push origin <branch_name>`  这会将本地分支推送到远程仓库`origin`下的同名分支。如果远程不存在该分支，Git 会自动创建它。

  * 设置上游分支关联:    执行`git branch --set-upstream-to=origin/<branch_name> <branch_name>`。例如，如果分支是`new_feature`，则执行`git branch --set-upstream-to=origin/new_feature new_feature`。这样就建立了本地分支和远程分支的关联。之后直接git push  则会自动推送

修改

* 从缓存中删除：git rm --cached  [filename]   ##把文件从暂存区域移除，但仍然希望保留在当前工作目录中，换句话说，仅是从跟踪清单中删除
* 将文件从暂存区和工作区中删除：git rm [filename]
* 强制删除：git rm -f  [filename]


标签

git tag <tag\_name>

通常遵循的命名模式如下：


通常遵循的命名模式如下：




<pre data-line="699"><section><span><span></span><span></span><span></span></span><span> </span></section><pre data-title="true"><code data-line="699"><span>v<span><</span>major<span>></span>.<span><</span>minor<span>></span>.<span><</span>patch<span>></span></span><br/></code></pre></pre>

* major（主版本号）：重大变化
* minor（次要版本号）：版本与先前版本兼容
* patch（补丁号）：bug修复
*
