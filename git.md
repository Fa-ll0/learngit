
分支管理，自定义git待更新
~~都说挺简单，这玩意儿学习周期好像也不短，学了一下午就学到分支管理呐。。。~~
source:https://www.liaoxuefeng.com/wiki/896043488029600/1317161920364578
廖雪峰的git教程
# GIT
>设计想法好机智，git就是来管理修改的
### 基础配置：
- 设置提交的用户信息：
git config --global user.name 'username'
git config --global user.email test@usr.com
##  基础命令：
- 创建版本库:
 git init//将当前目录变为repository仓库
- 文件添加到仓库：
git add \<file>
- 文件提交到仓库：
git commit -m \<message>
- 查看修改内容
git diff
- 查看状态
git status
>commit表示快照
## 版本控制：
- 查看日志
git log
- 版本回退
git reset --hard HEAD^/部分版本号（可以回到新版本）
>HEAD表示当前版本，每加一个^表示回溯一个版本，HEAD~100表示回溯100个版本
- 查看命令日志
git reflog（忘了版本号可以看看）
>原理：工作区->add->stage(暂存区）->commit->版本库的当前分支
- 撤销修改
>git checkout -- \<file>
  丢掉工作区的修改,复原工作区误删的文件--准确来说是用版本库的版本替换工作区的版本
>git reset HEAD \<file>   unstage，重新放回工作区
- 删除文件
git rm \<file>
git commit略（若先删除了文件，使用git add 和git rm一样）
>warnning:恢复文件只能恢复到最新版本
## 远程库：
1. git remote add **origin** git@github.com:Fa-ll0/learngit.git
本地内容推送到远程库
2. git push             将当前分支推送到远程，-u参数将本地和远程的master分支关联起来
3. git push origin master     将master的新修改推送到远程库
4. git remote -v     查看远程库信息
5. git remote rm origin 解除本地和远程库的绑定关系
6.  git clone git@github.com:Fa-ll0/learngit.git
克隆一个本地库(采用https://github.com/Fa-ll0/learngit.git亦可)
下载别人的代码只需要先fork一下即可
向官方库提供修改需要pull request
## 分支管理：
1.创建并切换到分支dev
- git checkout -b dev(==git branch dev git checkout dev)
- git switch -c dev(==git branch dev git switch dev)(新版本支持）
2.查看分支
git branch
3.合并分支dev
git merge dev
4.删除分支dev
git checkout -d dev
解决冲突
管理策略
bug分支
feature分支
多人协作
rebase
## 标签管理：
tag代表版本号，标记的是commit
git tag v1.0 （CommitId）          标记tag，不加默认为HEAD
git tag                                            查看所有tag
git tag -a \<tagname> -m "说明"  指定标签信息
git tag -d \<tagname>                    删除标签
git push origin \<tagname> (--tags)  推送本地标签到远程
git push origin :refs/tags/\<tagname>删除远程标签（应先删本地）
## 自定义的git：
## 可视化工具--sourcetree:
感觉暂时好像不大用的上，就先不学了




