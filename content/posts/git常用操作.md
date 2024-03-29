---
title: "git常用操作"
date: 2019-04-11T11:45:36+08:00
draft: false
---

设置你的用户名称与邮件地址

```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

检查你的配置

```
git config --list
```

初始化仓库

```
git init
```

提交

```
git add *.c
git add LICENSE
git commit -m 'initial project version'
```

克隆

```
git clone https://github.com/xxx/xxx
```

查看状态

```
git status
```

创建新分支

```
git branch testing
```

分支切换

```
git checkout testing
```

查看远程分支

```
git branch -a
```

查看本地分支

```
git branch
```