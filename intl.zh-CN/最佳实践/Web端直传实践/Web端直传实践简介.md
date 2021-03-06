# Web端直传实践简介 {#concept_iyn_vfy_5db .concept}

本教程介绍如何在Web端通过表单上传方式直接上传数据到OSS。

## 背景 {#section_m3m_xfy_5db .section}

每个OSS的用户都会用到上传服务。Web端常见的上传方法是用户在浏览器或app端上传文件到应用服务器，然后应用服务器再把文件上传到OSS。

![](http://static-aliyun-doc.oss-cn-hangzhou.aliyuncs.com/assets/img/4403/1459_zh-CN.png)

和数据直传到OSS相比，以上方法有三个缺点：

-   上传慢。先上传到应用服务器，再上传到OSS，网络传送比直传到OSS多了一倍。如果直传到OSS，不通过应用服务器，速度将大大提升，而且OSS采用BGP带宽，能保证各地各运营商的速度。
-   扩展性差。如果后续用户多了，应用服务器会成为瓶颈。
-   费用高。需要准备多台应用服务器。由于OSS上传流量是免费的，如果数据直传到OSS，不通过应用服务器，那么将能省下几台应用服务器。

## 目的 {#section_cym_wfy_5db .section}

本教程的目的是通过以下三个例子介绍如何通过表单直传数据到OSS：

-   [JavaScript客户端签名直传](intl.zh-CN/最佳实践/Web端直传实践/JavaScript客户端签名直传.md#)讲解在客户端通过JavaScript代码完成签名，然后通过表单直传数据到OSS。
-   [服务端签名后直传](intl.zh-CN/最佳实践/Web端直传实践/服务端签名后直传.md#)讲解在服务端通过PHP代码完成签名，然后通过表单直传数据到OSS。
-   [服务端签名直传并设置上传回调](intl.zh-CN/最佳实践/Web端直传实践/服务端签名直传并设置上传回调.md#)讲解在服务端通过PHP代码完成签名，并且服务端设置了上传后回调，然后通过表单直传数据到OSS。OSS回调完成后，应用服务器再返回结果给用户。

