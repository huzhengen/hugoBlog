---
title: "thinkphp5 验证码验证成功后 不管config文件里面有没有设置是否重置 实际都会重置 如何解决"
date: 2018-07-17T12:03:33+08:00
draft: false
---

解决办法：

文件目录下 .\vendor\topthink\think-captcha\src\Captcha.php

打开文件 直接在这个类库文件里面修改

'reset'     => false,