# 服务网格中间件

引文参照：

* [服务网格——什么是服务网格(CSDN) 原理1](https://blog.csdn.net/weixin_39734304/article/details/103756132)
* [服务网格——什么是服务网格(CSDN) 原理2](https://blog.csdn.net/weixin_39734304/article/details/103756152)

## 更多文章

* [使用 CloudMesh 轻松实践 Service Mesh](https://www.sofastack.tech/guides/kc-cloud-mesh-demo/)

## 定义

[Phil Calçado](http://philcalcado.com/) 在他的这篇博客 [Pattern: Service Mesh](http://philcalcado.com/2017/08/03/pattern_service_mesh.html) 中详细解释了服务网格的来龙去脉：

1. 从最原始的主机之间直接使用网线相连
1. 网络层的出现
1. 集成到应用程序内部的控制流
1. 分解到应用程序外部的控制流
1. 应用程序的中集成服务发现和断路器
1. 出现了专门用于服务发现和断路器的软件包/库，如 Twitter 的 Finagle 和 Facebook 的 Proxygen，这时候还是集成在应用程序内部
1. 出现了专门用于服务发现和断路器的开源软件，如 Netflix OSS、Airbnb 的 synapse 和 nerve
1. 最后作为**微服务的中间层服务网格**出现

## 优缺点

参读《微服务架构深度解析：原理、实践与进阶》



## 蚂蚁金服

在线预览 [蚂蚁金服-使用CloundMesh体验ServiceMesh.pdf](./asserts/蚂蚁金服-使用CloundMesh体验ServiceMesh.pdf)