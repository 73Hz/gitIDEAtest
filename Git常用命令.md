## Git常用命令

1. #### 环境配置

   1. 设置用户信息

      `git config --global user.name "kkt"`

      `git config --global user.email "159...@qq.com"`

   2. 查看配置信息

      `git config --list`

      `git config user.name`

2. #### 克隆

   1. `git clone 远程Git仓库地址`

3. #### Git工作目录下文件的两种状态

   1. untracked 未跟踪（未被纳入版本控制）
   2. tracked 已跟踪（被纳入版本控制）
      1. Unmodified 未修改状态
      2. Modified 已修改状态
      3. Staged 已暂存状态
   
4. #### 本地仓库操作

   1. ##### 加入暂存区以及提交()
   
      1. 加入暂存区
         1. git add
         2. -s   简洁表示
         3. "..."注释说明
      2. 提交
         1. git commit
         2. -m   简洁表示
         3. "..."注释说明
   
   2. ##### 创建文件
   
      touch加文件名及后缀
   
5. #### 远程仓库操作

   1. ##### 查看远程仓库

      1. `git remote -v`
      2. 更详细的信息：`git remote show origin`

   2. ##### 添加远程仓库

      1. `git remote add<shortname> <url>`

   3. ##### 从远程仓库克隆

      1. git clone <url>

   4. ##### 移除无效远程仓库

      1. git remove rm(从本地移除仓库的记录)
   
   5. ##### 从远程兄库中抓取与拉取
   
      1. 抓取 `git fetch`(不会自动merge)
      2. 拉取 `git pull`(从远程仓库中获取最新版本并merge到本地仓库)
      3. 合并 `git merge []`
   
   6. ##### 推送到远程仓库
   
      1. `git push [remote-name] [branch-name]`
   
6. #### 分支

   1. 查看分支
      1. 列出所有本地分支 `git branch`
      2. 列出所有远程分支 `git breanch -r`
      3. 列出所有本地以及远程分支 `git breanch -a`
   2. 创建分支
      1. `git branch [branch-name]`
   3. 切换分支
      1. `git checkout [branch-name]`
   4. 分支合并
      1. `git merge [想要合并的branch-name]（在主分支里执行）`