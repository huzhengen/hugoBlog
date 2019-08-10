---
title: "三条命令入门git"
date: 2018-10-03T16:06:11+08:00
draft: false
---

先写下这三条命令

* git init

* git add

* git commit -v

**git init**

![/images/git-intro-1.png](/images/git-intro-1.png)

比如先创建一个文件夹，从命令行进入该文件夹，在命令行输入`git init`，这样就会初始化一个仓库，会在该文件夹创建一个`.git`的目录

**git add**

![/images/git-intro-2.png](/images/git-intro-2.png)

把文件添加到`暂存区`，可以一个一个的添加，也可以一次添加N个。

**git commit -v**

![/images/git-intro-3.png](/images/git-intro-3.png)

![/images/git-intro-4.png](/images/git-intro-4.png)

输入`git commit -v`，会打开一个编辑器，你可以在里面详细的填写你都做了哪些修改。

![/images/git-intro-5.png](/images/git-intro-5.png)

> 默认打开的编辑器是vim，我不会vim，会直接按esc然后输入`:q!`退出。然后用`git commit -m`命令，m后面添加提交信息，比如`git commit -m "first commit"`。

运行了这三步，你的修改就被提交到了该仓库里。

[git中文文档](https://git-scm.com/book/zh)