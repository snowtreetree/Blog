# 浏览器地址栏输入URL

## 过程

### 校验网址格式、协议补齐

格式不正确的网站地址，检验通过后才会进到下一步。
用户访问的时候，很多是不会输入协议相关的内容，浏览器会自动补全，默认为HTTP。

### DNS解析

TCP/IP 协议中，必须要知道对应的IP地址，才能够建立连接（[链接](../blog/http/protocol.html#tcp-ip#DNS)）。

#### 查询路径

##### 1. 浏览器缓存

##### 2. 操作系统缓存

##### 3. hosts文件

##### 4. DNS服务器

先向`LDNS`本地域名服务器查询，查询不到的话，继续向根域名服务器发起查询请求，根域名服务器返回主域名服务器地址（比如.com,.cn等），然后本地服务区再向主域名服务器发起请求。

::: tip

DNS 劫持：域名劫持。

[dns-prefetch](https://zhuanlan.zhihu.com/p/22362198):
浏览器会对当前页面带有href的link的dns都prefetch一遍。

:::

### TCP握手

三次握手

### TLS握手

确定认证算法、加密算法、数据校验算法等，校验证书的有效性。

### TCP传输

### 服务器接收请求

处理请求或重定向等。重定向会导致重新走一遍上述流程。

### 服务器响应，客户端接收

客户端解压

### 渲染页面

### JS编译执行

## 参考

[在浏览器地址栏输入一个URL后回车，背后会进行哪些技术步骤？](https://www.zhihu.com/question/34873227)
