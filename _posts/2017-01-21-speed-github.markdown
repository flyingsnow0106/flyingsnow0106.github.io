---
layout: post
title:  "提高github的访问速度"
date:   2017-01-22
---
## 为什么访问速度慢？

这个原因就不用说了，你我都懂的，单单访问github主页还凑合，当然也有点慢。由于伟大的Q，对DNS解析进行污染，不管是访问还是`push`都会龟速。

## 如何提速？

绕过DNS解析，直接通过hosts解析，反正github一时半会也不会换IP地址。


记事本打开:

`C:\Windows\System32\drivers\etc\hosts`

最末尾添加两句话:

`151.101.72.249 http://global-ssl.fastly.Net`

`192.30.253.112 http://github.com`

添加后，访问主页速度快很多，`push`代码也快很多，感觉至少提速10倍
