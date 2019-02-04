
记录工作过程中遇到的有关 git 的操作和命令

---

参考：

[我怎么用git clone 远程的所有分支](https://zhidao.baidu.com/question/264071541339121645.html)

[git 分支管理 推送本地分支到远程分支等](https://blog.csdn.net/hijiankang/article/details/47254179)

[Book Pro Git](https://git-scm.com/book/zh/v1)

[Git教程-廖雪峰](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000)

[github/gitignore](https://github.com/github/gitignore)

[Android Studio中 .gitignore配置](https://blog.csdn.net/xiangzhihong8/article/details/54017831)

---

#工具下载#

[git](https://git-scm.com/downloads)

[TortoiseGit](https://tortoisegit.org/)

[Download Beyond Compare](http://www.scootersoftware.com/download.php)

---


查看 git 某一子命令的使用方法：git 子命令 --help

比如：git branch --help

git 官方文档：[Reference](https://git-scm.com/docs)

---

主要内容：

* 日志查看（git log）
* 文件操作（git add/commit/status）
* 本地分支操作（git checkout/branch）
* 远程分支操作（git checkout/branch/remote）
* 比较操作和分支合并操作（git diff/merge）
* 同分支不同版本操作

---

#日志查看（git log)#

参考：

[git-log - Show commit logs](https://git-scm.com/docs/git-log)

[git 使用详解（5）-- get log 查看提交历史](https://blog.csdn.net/wh_19910525/article/details/7468549)

* 查看当前分支日志
	
		git log

* 每条日志单行显示
	* git log --pretty=oneline
* 图形化显示提交合并历史
	* git log --graph
* 图形化显示并且每条日志单行显示
	* git log --graph --pretty=oneline
* 输出指定作者（author）的提交历史
	* git log --author="Author_Name"
* 输出提交日志中包含指定关键字
	* git log --grep="关键字"
* 同时查找指定作者以及指定关键字的日志
	* git log --grep="关键字" --author="" --all-match

**查看所有操作的命令**

	git reglog

---

#文件操作（git add/commit/status/checkout）#

* 首次添加文件到暂存区
	* git add 文件名
	* 如果有多个文件，可以一次性添加
		* git add *
* 将暂存区文件还原
	* git reset HEAD 文件名(可添加多个文件名，以空格隔开)
	* 同样对于多个文件，可以一次性还原
		* git reset HEAD *
* 将暂存区文件添加到版本库
	* git commit -m "添加日志信息"
* 还原暂存区或版本库修改的文件
	* git checkout -- 文件名(可添加多个文件名，以空格隔开)
* 查看当前文件状态
	* git status
* 回退文件到某一个版本
	* git reset --hard 版本号
	* 回退文件到最新版本
		* git reset --hard HEAD

*Note：暂存区或版本库文件被修改后需要重新添加*

---

#本地分支操作（git checkout/branch）#

* 查看当前分支
	* git branch（带星号的就是当前分支）
* 切换分支
	* git checkout 分支名
* 新建分支并切换
	* git checkout -b 分支名
* 

---

#远程分支操作（git checkout/branch/remote）#

* 下载远程仓库
	* git clone 远程仓库地址
* 查看远程仓库名
	* git remote
* 查看远程分支及本地分支
	* git branch -a
* 拉取远程修改到本地
	* git pull
* 推送本地修改到远程
	* git push

---

#比较操作和分支合并操作（git diff）#

参考：

[git-merge完全解析](https://blog.csdn.net/t3/article/details/77069523)

* 合并其他分支到当前分支
	* git merge 其他分支名
* 合并失败后恢复合并前的状态
	* git merge --abort
* 比较其他分支和本地分支
	* git diff 其他分支名
	* 



当前分支a合并另一个分支b

如何能够a仅合并b的修改，不合并b的历史

使用参数 --squash 即可

git merge --squash another

参考

[git merge –squash介绍](https://www.wanglianghome.org/2010/08/05/git-merge-squash/)

---

config 配置

全局配置文件路径

	/home/zhujian/.gitconfig

局部配置文件路径

---

Android Studio 配置 git

参考：[Android studio 如何查看当前git 分支的4种方式](https://blog.csdn.net/zhaoyanjun6/article/details/72284358)

如何查看当前所处分支：
	
---

同分支不同版本操作

回退到之前的分支

git reset --hard commit-id

从之前分支回到最新分支

git reset --hard commit-id



