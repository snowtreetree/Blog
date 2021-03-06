# 请求方法

请求方发出一个请求指令，接收方根据指令的方法及对应资源进行操作。PS请求方法都是大写。

## 常用方法

### GET

获取资源

### HEAD

获取资源的元信息，和GET类似，但是不会获取数据。

### POST

提交数据（写入、上传）

### PUT

和POST类似，多更新数据。

## 非常用方法

### DELETE

删除资源，危险性较大，服务器通常不会删除，会增加删除标识。

### CONNECT

建立特殊连接通道。web服务器充当代理，为客户端和另一台远程服务器建立一条特殊连接隧道。

### OPTIONS

列出可对资源实现的方法。在跨域的情况下，浏览器发起复杂请求的时候，会先发使用OPTIONS发起一个预检查请求（prelight request），从而判定服务器是否支持跨域。待确认好之后，才能够发起对应的复杂请求。

#### 简单请求（并不适用于Fetch）

`简单请求不会触发CORS预检请求。`

- 使用GET、POST、HEAD
- 人为设置Accept、Accept-Language、Content-Language、Content-Type等
- Content-Type 的值仅限于下列三者之一，text/plain，multipart/form-data，application/x-www-form-urlencoded
...

### TRACE

追踪请求 - 响应的传输数据。

## 安全、幂等

- 安全是指不会对服务器上的资源修改。GET、HEAD。
- 幂等，多次执行之后，效果都一样。POST是新增或提交数据，多次提交会创建多个资源，所以不是幂等。PUT，多次更新，资源还是第一次更新的状态，所以是幂等。
