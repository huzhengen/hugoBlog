---
title: "npm和yarn安装node-sass失败的完美解决方案"
date: 2019-02-27T19:28:34+08:00
draft: false
---

npm :

```
npm config set registry http://registry.npm.taobao.org
```

yarn :

```
yarn config set registry http://registry.npm.taobao.org
```

只指定node-sass的下载源：

npm：

```
npm config set sass-binary-site http://npm.taobao.org/mirrors/node-sass
```

yarn：

```
yarn config set sass-binary-site http://npm.taobao.org/mirrors/node-sass
```