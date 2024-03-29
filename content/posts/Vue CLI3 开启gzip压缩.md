---
title: "Vue CLI3 开启gzip压缩"
date: 2019-02-27T19:28:34+08:00
draft: false
---

首先`yarn add compression-webpack-plugin -D`或者用npm

然后在vue.config.js文件里添加代码

```js
const CompressionPlugin = require("compression-webpack-plugin")

module.exports = {
	configureWebpack: config => {
        if (process.env.NODE_ENV === 'production') {
            return {
                plugins: [
                    new CompressionPlugin({
                        test: /\.js$|\.html$|\.css/,
                        threshold: 10240,
                        deleteOriginalAssets: false
                    })
                ]
            }
        }

    }  
}
```

然后`yarn build`就可以了，在dist目录里的css、js会出现对应的.gz的文件。

同时服务器也要开启gzip

nginx开启的话，修改ngix.conf文件

```
gzip  on;
gzip_types text/plain application/x-javascript application/javascript text/css application/xml text/javascript application/x-httpd-php image/jpeg image/gif image/png;
```