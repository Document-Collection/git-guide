
# remote: error: cannot lock ref 'refs/heads/master': ref refs/heads/master

在`Travis CI`上上传文件到远程仓库，出现如下问题

    remote: error: cannot lock ref 'refs/heads/master': ref refs/heads/master

## 起因

我在上传提交时中间中断了

    $ git push -u origin dev
    Counting objects: 6, done.
    Delta compression using up to 8 threads.
    Compressing objects: 100% (6/6), done.
    Writing objects: 100% (6/6), 556 bytes | 0 bytes/s, done.
    Total 6 (delta 5), reused 0 (delta 0)
    remote: Resolving deltas: 100% (5/5), completed with 5 local objects.
    ^C

然后再更新文章后再一次提交，就出现了远程仓库锁定的问题

## 解决

参考：[git: error: cannot lock ref, error: cannot lock ref](https://blog.csdn.net/sinat_36246371/article/details/79959598)

将远程仓库下载到本地，然后执行如下命令

    git remote prune origin

其作用是同步本地远程分支，删除本地已过时的远程分支

重新触发`CI`工具执行，此时能够成功更新了