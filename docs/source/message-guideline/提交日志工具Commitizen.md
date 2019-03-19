
# 提交日志工具Commitizen

[Commitizen](http://commitizen.github.io/cz-cli/)是一个提交日志工具，辅助开发者使用提交规则

## 预配置

首先需要安装NodeJS，参考：[nodeJS安装](https://hexo-guide.readthedocs.io/zh_CN/latest/node/nodeJS%E5%AE%89%E8%A3%85.html)

其次需要对仓库进行`Node`初始化，生成`package.json`文件

    $ npm init -y

## 安装`Commitizen`

    # 全局安装
    $ npm install -g commitizen

### 测试

安装完成后，使用`git-cz`替代`git commit`完成提交操作，

    $ git cz
    cz-cli@3.0.7, cz-conventional-changelog@2.1.0
    ...
    ...

通过提示信息辅助你完成标准化的提交日志

**`git-cz`支持`git commit`所有的参数设置**

## 安装`Adapter`

`Commitizen`支持多种不同的提交规范，可以安装和配置不同的适配器实现

以`Conventional Commit`规范为例

### 全局配置

    # 安装
    $ npm install -g cz-conventional-changelog
    # 配置
    $ echo '{ "path": "cz-conventional-changelog" }' > ~/.czrc

### 本地配置

    # 安装
    commitizen init cz-conventional-changelog --save-dev --save-exact

安装完成后除了下载`cz-conventional-changelog`包外还在`package.json`中添加了

    ...
    "config": {
        "commitizen": {
            "path": "cz-conventional-changelog"
        }
    }

## 徽章

在`README`中添加`commitizen`友好徽章

[![](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)