
# git配置

## 配置文件

git有3个级别的配置文件：

1. local：本地文件存放在仓库中(.git/config)，只针对当前仓库
2. global：全局文件存放为`~/.gitconfig`或`~/.config/git/config`，作用于当前用户的所有仓库
3. system：系统文件存放为/etc/gitconfig，作用于系统的每个用户

其优先级为local > global > system

*`windows`环境下的全局配置文件存放为`C:\\User\\$USER\\.gitconfig`*

## 设置配置信息

使用命令`git config`进行配置，各级别设置需要加上可选参数

    git config --system ...
    git config --global ...
    git config --user ...

### 设置用户信息

每次提交时都需加上用户名和邮箱地址，可以设置成全局变量

    git config --global user.name user-name
    git config --global user.email email-address

### 设置文本编辑器

git使用系统默认的编辑器，可以设置指定编辑器

    git config --global core.editors code

### 打印配置信息

    zj@zj-ThinkPad-T470p:~$ git config --list
    user.email=505169307@qq.com
    user.name=zhujian
    core.editor=code




