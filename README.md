# gitdemo
git practice field

## git练习实践

### 一、克隆远程仓库到本地——git clone

> git clone url

### 二、提交新建文件到远程仓库

~~~shell
$ git status   #显示工作目录和暂存区的状态
$ git add .    #添加所有新建文件到暂存区
$ git status   #显示工作目录和暂存区的状态
$ git commit -m "提交注释信息"   #将暂存区代码提交到本地仓库的相应分支
$ git status   #显示工作目录和暂存区的状态
$ git remote add origin 仓库地址	#没有绑定远程仓库或克隆项目，需要绑定一下。若绑定或已克隆，可忽略这一步
$ git push origin 分支名     #将本地仓库的分支推送到远程仓库相应分支下
~~~

### 三、修改本地代码，在提交到远程仓库

~~~shell
$ git status
$ git add ./目录名/文件名   或   git add .   #前一个命令是提交单个新建文件到暂存区，如果文件提交文件过多，建议使用第二个命令，第二个命令是提交所有新建文件到暂存区
$ git status
$ git commit -m "提交注释信息"
$ git push origin 分支名
~~~

### 四、拉去远程仓库，同步本地仓库

~~~shell
$ git pull	#拉去代码
$ git pull origin 分支名	#拉取远程仓库制定分支到本地仓库的相应分支
~~~

> **注意：**git pull是git fetch与git merge 的组合，git pull执行的顺序是先git fetch，后git merge。如果拉去失败，可以使用强制拉取，命令如下：
>
> ~~~shell
> git fetch --all						#覆盖该分支所有代码
> git reset --hard origin/分支名		  #强制重置
> git pull							#拉取到本地
> ~~~
>
> **注意：**reset比较暴力，相当于 可适用于 代码在工作区、暂存区、仓库区等任何场景，重置后不可恢复🙅‍♂️，对于新手有一定的安全隐患。

