# 比较 gRPC 服务和 HTTP API

## 引文

* [微软文档关于《gRPC 服务和 HTTP API》的差异](https://docs.microsoft.com/zh-cn/aspnet/core/grpc/comparison?view=aspnetcore-5.0)
* [Google开源的gRPC站点](https://opensource.google/projects/grpc)
* [gRPC 编程](https://www.grpc.io/)

## gRPC

`gRPC`是谷歌开源的一个 RPC 框架，面向移动和 `HTTP/2` 设计。

* 内容交换格式采用`ProtoBuf(Google Protocol Buffers)`，开源已久，提供了一种灵活、高效、自动序列化结构数据的机制，作用与XML，Json类似，但使用二进制，（反）序列化速度快，压缩效率高。
* 传输协议 采用`http2`，性能比`http1.1`好了很多
* 和很多RPC系统一样，服务端负责实现定义好的接口并处理客户端的请求，客户端根据接口描述直接调用需要的服务。客户端和服务端可以分别使用gPRC支持的不同语言实现。

`ProtoBuf` 具有强大的`IDL`（interface description language，接口描述语言）和相关工具集（主要是protoc）。用户写好.proto描述文件后，protoc可以将其编译成众多语言的接口代码。

## HTTP/2

* 新的二进制格式:
  > HTTP1.X都是基于文本解析，而因为文本表现形式的多样性，基于文本协议的格式解析天然存在健壮性问题。而采用二进制格式后实现方便且健壮。
* 多路复用
  > 多个request共享一个连接。
* header压缩
  > 在HTTP1.x中header信息很多，且每次都会重复发送，造成很大浪费。HTTP2.0使用encoder减少了传输的header大小，且通信双方都缓存一份包含了header信息的表，此后的请求可以只发送差异数据，避免信息的重复传输，进一步减少需要传输的内容大小。
* 服务端推送
  > 主要的思想是：当一个客户端请求资源X，而服务器知道它很可能也需要资源Z的情况下，服务器可以在客户端发送请求前，主动将资源Z推送给客户端。这个功能帮助客户端将Z放进缓存以备将来之需。也遵守同源策略，且客户端可以拒绝推送过来的资源。
