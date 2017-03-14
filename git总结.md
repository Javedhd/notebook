![git](https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1489499470770&di=42f4885fcaf0917071d04797a3d89226&imgtype=0&src=http%3A%2F%2Fimages.cnblogs.com%2Fcnblogs_com%2Fqyf404%2F612381%2Fo_git-logo.png)
# git
Git是一款免费、开源的分布式版本控制系统，用于敏捷高效地处理任何或小或大的项目。
1. Git的读音为/gɪt/。Git是一个开源的分布式版本控制系统，可以有效、高速的处理从很小到非常大的项目版本管理。
2. Git 是 Linus Torvalds 为了帮助管理 Linux 内核开发而开发的一个开放源码的版本控制软件。
    Torvalds 开始着手开发 Git 是为了作为一种过渡方案来替代 BitKeeper，后者之前一直是 Linux 内核开发人员在全球使用的主要源代码工具。
    开放源码社区中的有些人觉得BitKeeper 的许可证并不适合开放源码社区的工作，因此 Torvalds 决定着手研究许可证更为灵活的版本控制系统。
    尽管最初 Git 的开发是为了辅助 Linux 内核开发的过程，但是我们已经发现在很多其他自由软件项目中也使用了 Git。
    例如 很多 Freedesktop 的项目迁移到了 Git 上。

# git安装
1. ubuntu linux 安装方法：
```sh
sudo apt-get install git
```
2. Mac ox 安装方法：
```sh
brew install git
```

# 创建git本地仓库
```sh
mkdir git
cd git
mkdir c
cd c
git init
```

# 增加文件
1. 复制已有的文件到当前目录里：
```sh
cp ../../c/*.c .
```
2. 创建一个新的文件。
```sh
touch hello.c
vim hello.c   //输出hello world字符串的C语言的程序（代码）
```
# 查看目录状态
查看当前目录下的文件在git仓库中的状态。
```sh
git status
```

# 跟踪文件
将当前目录下的所有文件， 进行跟踪。
```sh
git add .
```
# 配置个人用户信息
为提交增加个人用户信息。
```sh
git config --global user.name "Javedhd"
git config --global user.email "Javed.Shi@outlook.com"  
git config --global core.editor vim //设置默认编辑器为vim
```

# 提交
向本地git仓库提交， 跟踪文件。
```sh
git commit
```
提交信息
```````
First commit

Init commit.
```````

# 查看提交信息
查看提交相关信息。
```sh
git log
```
vim显示的信息
* 第一行： commit ID
* 第二行： 提交作者名子和email.
* 第三行： 提交的时间
* 第四行： 提交信息标题
* 第五行： 提交信息具体内容

# git diff
1. 查看修改源码。
```sh
git diff
```
2. 两个提交版本之间做比较
```sh
git diff  commitID-1 commitID-2
```
3. 理解Patch标记格式的含义。

# 删除文件
1. 删除文件后， 恢复文件。
```sh
rm -rf hello.c
git status
git checkout hello.c
```
2. 从版本库里删除文件。（真正删除文件）
```sh
git rm hello.c
```
或者
```sh
rm hello.c
git status
git add .
git commit
```

# 版本之间切换
根据commitID， 可以进行版本切换。
```sh
git reset --hard commitID
```

# 忽略文件
忽略不需要跟踪到git仓库里的文件。
```sh
touch .gitignore
vim .gitignore
```
vim编译器内容:
```
a.out
```
继续执行
```sh
git add .
git commit
```

# github
1. 注册github帐号
*  注册邮箱， 注意不要使用QQ.com

![git_signup](https://github.com/Javedhd/notebook/blob/master/img/git_signup.png?raw=true)

2. 创建gitc仓库
3. 从github将创建的gitc仓库， 克隆到本地。
```sh
git clone https://github.com/username/gitc.git
```
4. 将本地仓库与github仓库进行同步， 将本地提交推送到服务器上。
```sh
git push origin master
input username:
input password:
```
5. 更新本地仓库， 与github仓库进行同步。将服务器提交拉取到本地。

# 参考文献
[ro Git book zh](https://git-scm.com/book/zh/v2)

# 速查表
[](https://github.com/Javedhd/notebook/blob/master/img/git%E9%80%9F%E6%9F%A5%E8%A1%A8.jpeg?raw=true)
