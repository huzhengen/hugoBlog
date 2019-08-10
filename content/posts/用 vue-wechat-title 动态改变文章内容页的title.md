---
title: "用 vue-wechat-title 动态改变文章内容页的title"
date: 2019-01-02T09:10:14+08:00
draft: false
---

默认你的router.js已经写好了

```
npm install vue-wechat-title --save
```

配置main.js
```js
import VueRouter from 'vue-router'
import VueWechatTitle from 'vue-wechat-title'
import router from './router.js'
Vue.use(VueRouter)
Vue.use(VueWechatTitle)

router.beforeEach((to, from, next)=>{
    if(to.meta.title){
        document.title = to.meta.title
    }
    next()
})
```

然后在文章内容页第一个`div`上加`v-wechat-title="this.title"`
```js
data(){
    return {
        title: '文章123'
    }
}
```

来源：http://www.xdx97.com/#/single?bid=dbb4c713-85d9-7feb-f906-92bbbcb86ce3