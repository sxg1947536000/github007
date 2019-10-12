## 1初始化git仓库
### 在项目目录里面右键bash here
    - 第一步：git init
    - 第二步：在项目目录中新建文件。

## 2自报家门
### 就是在git中设置 自报家门，每一次备份都会讲当前备份者的信息存储起来。
- git config --global user.name  "sxg"   //设置名称
- git config --global user.email "sxg1947536000@gmail.com"  //设置邮箱

## 3把大象放进冰箱
### 1打开冰箱门
### 2放入

## 把代码存储到 .git中
文件--------大门口------仓储（把文件放到仓库的门口，把仓库门口的放到里面的房间中）

git add ./readme.md    //代码放进大门口
git commit -m "我们完成第一个功能" //把大门口的东西放进仓库 -m是做说明的意思（添加东西的说明。）/commit是提交的意思。

修改一次，add一次，commit一次。

## 4查看状态---查看修改的文件是否被修改
- 命令 `git status`  //查看当前的状态


## 5添加或者修改多个文件   git add ./          //一次性把多个文件放入暂存区


## 6一次性放入房间   
- git commit --all -m "往房间中一次性放入所有文件"  //---all（表示把所有修改过的文件放入仓储）

## git中的忽略文件
git log   //查看提交记录

---
接下来继续学习

准备第二次提交

开始提交

第一部检验状态  git status

发现有文件修改了，没有提交。

ok 开始使用代码进行提交 git add ./readme.md  放入了暂存区

继续看状态  git status

发现没有进行提交。。。

ok 进行提交   git  commit  -m "这个提交的内容主要是对git的命令进行了熟悉。"

---

查看记录，并且不断进行练习时很有必要的。

我们必须经常分析我们的代码，我们才能更好的掌握编程语言，虽然我们现在的能力不是很优秀，但是坚持学习，我们总是会有所收获，获得自己的成功。

---

通过命令查看日志

- `git log`查看完整版日志

- `git log --oneline  `查看间接版日志

  

###  git 代码的回退

查看版本

`git log`

`git reset  --hard head~0`  //回退版本，0的话，是回退一次，1是回退两次。

### git 切换制定版本

git reset --hard 【文件提交时的版本号】  / 

`git reflog`     //可以看到每一次切换版本的记录，可以看到所有提交的版本号

### 分支

- 默认有一个主分支
- `git branch dev`创建了一个dev分支,刚创建时dev分支里的东西和master分支里的东西是一样的
- `git checkout dev` 切换到指定的分支，这里切换到名为dev的分支【checkout却换】
- `git branch`可以查看当前有哪些分支

#### 合并分支

`git merge dev`合并分支内容，把当前分支与指定分支相结合（dev），进行合并

当前分支指的是`git branch`命令输出的前面有*星号的分支

### git hub

- https://github.com
- 不是git，只是一个网站

连接远程服务器：

- 初次连接时需要进行ssh密钥  `ssh-keygen -t rsa -C "1947536000@qq.com" `连续按3次回车，即可得到密钥。“id_rsa.pub”这个文件保存在c盘下面，找到它，用记事本打开后，复制密钥。
- 打开github.com网址，在个人中心，setings是部分找到SSH and GPG keys ，点击New ssh Key即可。
-  3.验证是否成功，在git bash里输入下面的命令
  `ssh -T git@github.com`
- 4.出现`You've successfully authenticated, but GitHub does not provide shell access.`表示成功。

### 上传文件

- git push 【上传仓库的url】master    //master表示讲本地文件上传到服务器仓库的master分支下面。