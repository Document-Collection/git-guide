
git 远程分支和本地分支管理

如何下载远程分支的代码到本地

如何在本地创建新分支

如何在本地新分支下载远程分支

如何将本地分支提交到远程分支

---

推送本地分支到远程分支

git push origin 本地分支:本地分支

比如：

git push origin zj_test:zj_test

如何查看本地分支是否已经和远程分支进行关联 (hook - 钩子)

如果切换本地分支和远程分支的关联，即本地分支是否可以切换不同的远程分支

git branch 	--set-upstream dev origin/dev

git push origin branch-name

git branch --set-upstream branch-name origin/branch-name

---

比较两个版本或者两个文件内容差异：git diff

比较同一分支同文件不同版本的差异

比较待提交的文件和已版本化的文件的差异

比较不同分支同文件的差异

---

如何添加 .gitignore 文件和在 AS 上使用 .gitignore 文件

https://github.com/github/gitignore

设置命令别名（alias）

git config --global alias st status

---

git 中指针 HEAD / master / origin 的意义和作用

fetch / push 的作用

---

git 关键名词：工作区（Working Directory）/ 版本库（Repository）/ 暂存库 / 

---

删除已版本化的文件 git rm 再 git commit -m "相应信息"

---

git 对于二进制文件的管理

直接使用 git 管理二进制文件，每次都会保存全部的二进制文件，而不是保存修改部分

---

使用 beyond compare 对比工具进行 git 比对（可配置）

beycond compare 官网地址：[http://www.scootersoftware.com/index.php](http://www.scootersoftware.com/index.php)

linux 安装：[Linux Installation Instructions](Linux Installation Instructions)

linux 自带 meld 了，还不错

---

分支合并后会将日志记录也合并进来吗？

保留合并的信息日志 git merge --no-ff 

fast forward 模式

---

远程信息查看

git remote 

git remote -v

git remote add

git remote rm

本地库连接多个远程库

---

git 标签（tag）的意义和使用

---

远程仓库：pull request

指定远程库分支合并到本地

git pull <remote> <branch>

git branch --set-upstream-to=origin/<branch> 本地分支名

---

[SSH公钥登录原理](https://www.cnblogs.com/scofi/p/6617394.html)

[SSH简介及公钥、私钥的基本概念](https://blog.csdn.net/l464373218/article/details/51280078)

---

[git merge的参数--squash的用处](https://blog.csdn.net/rockrockwu/article/details/33740711)

[.6 Git 工具 - 子模块](https://git-scm.com/book/zh/v1/Git-%E5%B7%A5%E5%85%B7-%E5%AD%90%E6%A8%A1%E5%9D%97)

[7.7 Git 工具 - 重置揭密](https://git-scm.com/book/zh/v2/Git-%E5%B7%A5%E5%85%B7-%E9%87%8D%E7%BD%AE%E6%8F%AD%E5%AF%86)

---

比较修改文件和最新版本的不同

比较暂存区文件和最新版本的不同

比较不同版本的文件不同

比较不同分支的文件不同

不叫不同分支的不同版本的文件不同

---

git commit 内容检查/关键字检查

git difftool 如何查看暂存区文件、如何查看修改文件

本地新建分支并推送到远程仓库（远程没有该新分支的情况下）

--

如何在 git commit 之前强制提交日志，强制日志规范

如何在推送之前强制检测文件

使用钩子（hook）

位于 .git/hook 文件夹下

[自定义 Git - Git挂钩](https://git-scm.com/book/zh/v1/%E8%87%AA%E5%AE%9A%E4%B9%89-Git-Git%E6%8C%82%E9%92%A90)

[Android Studio项目gradle+Git Hooks 实现提交时对提交日志和代码(checkStyle)的检查](https://www.jianshu.com/p/4e7280509636)

[五分钟内用Python实现GitHook](https://www.jianshu.com/p/f049cd1c44bc)

[使用 Githook 实现团队 Coding Review 流程](https://www.jianshu.com/p/935409ce4c9a)

使用 python 文件写

SyntaxError: Non-ASCII character '\xe5' in file .git/hooks/pre-commit on line 8, but no encoding declared; see http://python. org/dev/peps/pep-0263/ for details

--

比较两个commit的git修改

---

git 分支改名

git branch -m new_branch_name

git 删除分支

git branch -D branch_name

