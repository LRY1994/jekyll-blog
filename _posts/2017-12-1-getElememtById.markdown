---
layout: post
title:  "IE使用getElementById会抓到name"
date:   2017-12-1 09:24:38 +0800
img: "a.jpg"
tags: [programing]
---

昨晚在公司的OA系统提交账务报销的时候，发现保存老是保存不了，看了控制台，console出现了错误，OA是以前的老系统，用原生的js写的。具体原因是 document.getElementById(xx)取不到值。（我的OA只能用IE打开==）

然后去检查元素看了一下，发现并没有id==xx的元素，都是写成name=xx,当时我理所应当地以为是OA有bug,手动在name=xx的后面加上id=xx,再点击保存就OK了。

今天查了一下，原来不是有bug。

  >在 IE6 IE7 IE8(Q) 中，支持以 document.getElementById(elementName) 的方式获取 A APPLET BUTTON FORM IFRAME IMG INPUT MAP OBJECT EMBED SELECT TEXTAREA 元素，而其他浏览器的任何元素均不支持该方式。


参考

[SD9001: IE6 IE7 IE8(Q) 中的 getElementById 方法能以 name 属性为参数获取某些元素](http://www.w3help.org/zh-cn/causes/SD9001)

实验了一下，用IE8版本，成功了吼吼吼
