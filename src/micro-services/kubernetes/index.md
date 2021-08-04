# Kubernetes

## 官方网站

[https://kubernetes.io](https://kubernetes.io)

## 中文

* [Kubernetes 官方文档中文版](https://kubernetes.io/docs/home/)
* [Kubernetes 中文社区](https://www.kubernetes.org.cn/)
* [https://kuboard.cn/](https://kuboard.cn/)
  * 源码已经备份到 https://github.com/lauer3912/kuboard-press
  * 在线Demo: [https://demo.kuboard.cn/](https://demo.kuboard.cn/), 用户名及密码: demo/demo123

## 架构图及关键术语

参见 [复习Kubernetes核心概念](https://kuboard.cn/learning/k8s-basics/k8s-core-concepts.html)

## 安装

### 基于WSL2和Kind或Minikube：搭建Windows版Kubernetes

参见：[https://www.kubernetes.org.cn/7723.html](https://www.kubernetes.org.cn/7723.html)

## 常用术语

* `CRD`：CustomResourceDefinition, 在 Kubernetes 中一切都可视为资源，Kubernetes 1.7 之后增加了对 CRD 自定义资源二次开发能力来扩展 Kubernetes API，通过 CRD 我们可以向 Kubernetes API 中增加新资源类型，而不需要修改 Kubernetes 源码来创建自定义的 API server，该功能大大提高了 Kubernetes 的扩展能力。参考：[https://www.jianshu.com/p/cc7eea6dd1fb](https://www.jianshu.com/p/cc7eea6dd1fb) 或 [https://kubernetes.io/zh/docs/tasks/extend-kubernetes/custom-resources/custom-resource-definitions/](https://kubernetes.io/zh/docs/tasks/extend-kubernetes/custom-resources/custom-resource-definitions/)
