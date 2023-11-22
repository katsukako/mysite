# git

## 基础

> 我设置的用户名是katsu，邮箱是katsukako668@gmail.com(本地设置，不影响github)

1. vs code 中Command + Shift + P，然后输入"Git

2. 查看提交历史：Command + Shift + G然后点击源代码管理视图中的提交历史按钮

3. 解决冲突：在源代码管理视图中，选择冲突的文件，然后按Option + Enter，使用内置的冲突解决工具

## 基础命令

初始化本地库：

`git init`

???+ 提示

    katsu@JIAHAOnoMacBook-Air test % git init

    提示：使用 'master' 作为初始分支的名称。这个默认分支名称可能会更改。要在新仓库中配置使用初始分支名，并消除这条警告，请执行：

    提示：	git config --global init.defaultBranch <名称>
    
    提示：除了 'master' 之外，通常选定的名字有 'main'、'trunk' 和 'development'。可以通过以下命令重命名刚创建的分支：

    提示：	git branch -m <名称>

查看本地库状态：

`git status`

添加到**暂存区**：

`git add file_name`

???+ "删除暂存区文件"

      （使用 "git rm --cached <文件>..." 以取消暂存）

提交到**本地库**：

`git commmit -m"日志信息"文件名`

查看历史记录：

`git reflog`

版本穿梭：

`git reset --hard version_name`

## 分支的操作

创建分支：

`git branch branch_name`

查看分支：

`git branch -v`

切换分支：

`git checkout branch_name`

合并到当前分支：

`git merge branch_name`

???+ warning "合并冲突"

    当两个分支相同文件同一行或相邻行有不同修改时，自动合并会报错，合并冲突文件commit时，不能再带上文件名

## github

[github](https://github.com/)

查看当前所有远程地址别名：

`git remove -v`

起别名：

`git remove add nickname remote_address`

推送：

`git push nickname branch_name`

!!! note "推送"

    需要指定分支，换句话说最小单位是分支

克隆：

`git clone remote_address`

拉取且合并：

`git pull remote_nickname remote_branch_name`