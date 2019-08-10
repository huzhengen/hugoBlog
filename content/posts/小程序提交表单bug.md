---
title: "小程序打开的时候获取app.globalData为空"
date: 2018-11-22T13:46:29+08:00
draft: false
---

> 该博客只适合本人，我写的很简单，别人有可能看不懂描述。

小程序2个input，1个提交按钮。IOS测试，输入完成后，点击空白，然后再点提交，根本没反应。如果再点进去input，再点提交才可以。google后说确实有这个bug，没找着解决方法。

```html
<form bindsubmit="formSubmit" bindreset="formReset">
  <view class="section">
    <view class="section__title">input</view>
    <input name="input1" placeholder="please input here" />
  </view>
  <view class="section">
    <view class="section__title">input</view>
    <input name="input2" placeholder="please input here" />
  </view>
  <view class="btn-area">
    <button formType="submit">Submit</button>
    <button formType="reset">Reset</button>
  </view>
</form>
```

解决方法是：不用formSubmit。

当用户输入的时候用input的bindinput属性，检测用户的输入，同时用this.setState()保存用户的输入，提交的时候用this.data获取刚才用户的输入，然后提交表单。