# Git常用命令
git config --global user.name
git config --global user.email
git init
git status
git add <file>
git commit -m ""
git reflog
git log
git reset --hard <version> 切换版本
设置签名的作用是区分操作者身份，与远程仓库没有任何关系
ll 查看当前文件
ll -a 查看当前隐藏文件
本地文件 add-》暂存区 commit-》本地库
# branch
git branch -v
git branch <branch-name>
git checkout <branch-name>
git merge <branch-name>
合并冲突：当同一个文件同一个位置发生冲突，需要自己在文件中编辑冲突的代码
# 远程库
内部团队
+ 公开的项目是可以随意clone的
+ 但是想要push，需要作者的邀请
跨团队
+ 跨团队时，获取代码库，需要fork过来，然后在自己的团队内部进行开发
+ 开发完毕后，发送pull request请求，通知原团队
+ 原团队审核一下后就可以merge了，pull下来更新一下本地库，就可以继续在内部开发了
# 远程库
git remote -v
git remote add <url别名> <url> 建立远程库连接并起别名
git push <url别名> <本地分支名> 推送本地分支的内容到远程库
git clone <url别名> 克隆:拉取数据=》init本地库=>创建url别名
git pull <url别名> <远程分支名> 拉取指定分支的数据，并与本地合并
git checkout -b 分支名称 创建并切换分支（和远程仓库的分支名一致才能push）
git checkout -b <新分支名> <被克隆的分支> 克隆分支并切换到新分支
git branch -a 查看远程所有分支
# SSH免密码
解决windows的身份验证
ssh-keygen -t rsa -C "bidongyu15@outlook.com"
.ssh 文件夹里就是


