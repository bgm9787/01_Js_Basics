#### git---分布式的版本管理系统 

**工作区(working directory)，**就是工作的区域（本地工作目录），工作区的内容会包含提交到暂存区和版本库(当前提交点)的内容，同时也包含自己的修改内容。

**暂存区(stage area, 又称为索引区index)**，git add命令将工作区内容添加到暂存区。在工作目录下有一个.git的目录，里面有个index文件，存储着关于暂存区的内容。

**本地仓库(local repository)，**版本控制系统的仓库，存在于本地。当执行git commit命令后，会将暂存区内容提交到仓库之中。

**远程仓库(remote repository)，**存在远程，可用于远程协作，通过push/pull/fetch可实现本地与远程的交互



#### 关于远程仓库

- 查看当前远程地址  `git remote -v`
- 删除当前远程地址   `git remote rm origin`
- 添加新远程地址       `git remote add origin 远程仓库地址`



#### 关于分支

- 查看当前分支		     `git branch`  （git branch -a   包括远程分支）

- 新建分支(本地)		   `git branch 分支名`

- 切换分支                     `git checkout 分支名`

- 在本地新建分支并切换（相当于以上两条命令）     `git checkout -b 分支名`

- 删除分支                      `git branch -d 分支名`

- 在github远程端删除一个分支           `git push origin :newbranch` (分支名前的冒号代表删除)

- 将新的分支推送到github                   `git push origin newbranch`

- 分支的优势：

  - 分支 ----- 可以写小demo，测试用，同时避免破坏原代码结构
  - 分支 ----- 便于多人协作开发，分别完成不同功能，最后合并，更高效开发

  - 分支 ----- 便于解决线上bug，eg: 正在dev分支写新需求，线上master环境出现bug，可从maste拉取代码，既能及时解决问题并及时上线，又不会破坏已完成部分新需求

  - 分支 ----- 便于比较不同分支差异，修改/新增了什么 

  

#### 提交代码操作

```
git status   （随时检查文件状态）
git add .        （把要提交的所有修改放到暂存区（Stage））
git commit -m ""  （把暂存区的所有修改提交到本地分支）
git push -u origin dev   （提交到远程）
```



#### 本地代码推送到远程仓库

```
1. 首先创建一个远程仓库
3. git init 初始化本地git仓库配置
4. git remote add origin [远程仓库地址] 添加远程仓库
5. git add . 添加工作区代码到本地暂存区
6. git commit -m " [提交描述]" 添加暂存区代码到本地仓库
7. git pull origin master 将远程仓库pull下来
8. git push -u origin master 将代码push到远程仓库master分支。
```



#### 撤销操作

场景1：当你改乱了工作区某个文件的内容，想直接丢弃工作区的修改时，用命令。

```
git checkout -- file
```

场景2：当你不但改乱了工作区某个文件的内容，还添加到了暂存区时，想丢弃修改，分两步，第一步用命令``git reset HEAD ``，就回到了场景1，第二步按场景1操作。

```
git reset HEAD
```

场景3：已经提交了不合适的修改到版本库时，想要撤销本次提交， 

```
git reset --hard HEAD^  //撤销回到上个版本
$ git reset --hard 1094a  // 回滚具体某个版本
```

 Git提供了一个命令`git reflog`用来记录你的每一次命令，要重返未来，用`git reflog`查看命令历史，以便确定要回到未来的哪个版本。



#### 分支合并

```
举例：git dev分支合并到master并提交
    git branch    //查看当前版本
    git checkout dev  // 如果当前在dev分支上面 则不用执行 如果不在dev 则执行
    git pull   // 拉取最新的代码
    git checkout master  //切换到master分支上面
    git pull  //确保最新的代码
    git merge dev  //将dev分支上面的代码合并到master
    git push origin master // 推送到远程master仓库
```



#### 其他命令

- git clone  远程仓库地址    第一次拿远程的代码
- git diff   比较工作目录和暂存区域快照之间的差异，也就是修改之后还没有暂存起来的变化内容
- git log   显示日志
- git rm 文件名  ----- 移除某文件
- git mv 原文件名 新文件名  ----- 移动某文件 （相当于一下三句命令）
  - mv oldFile newFile
  - git rm oldFile
  - git add newFile

```console
cat .gitignore
```



#### 其他场景

- 将远程dev分支拉取到本地test    `git fetch origin dev：test`
- 将本地的abc分支推送到远程dev        `git push origin abc：dev`
- 在项目中想要过滤（忽略）read文件   `vim .gitignore`(新增.gitignore文件并在其中加入read文件名)

注意：使用fech获取时，并未合并到本地仓库，此时可使用git merge实现远程仓库副本与本地仓库的合并；；pull命令是拉取代码并合并到本地仓库。我们尽可能使用fetch命令更加保险。



rebase













