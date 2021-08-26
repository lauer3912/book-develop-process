# Allure 测试报告查看器

## 前言

Allure 是由Qameta Software团队开源的一款旨在于解决让每个人能更容易生成并更简洁阅读的测试报告框架。它支持大多数的测试框架，如：JUnit、Pytest、TestNG等，简单易用便于集成。

## 安装

参照官方文档：[https://docs.qameta.io/allure/#_installing_a_commandline](https://docs.qameta.io/allure/#_installing_a_commandline)

### Linux

```bash
# debian-based PPA
sudo apt-add-repository ppa:qameta/allure
sudo apt-get update 
sudo apt-get install allure
```

手动安装，参见 [https://docs.qameta.io/allure/#_manual_installation](https://docs.qameta.io/allure/#_manual_installation)

### Windows

```cmd
scoop install allure
\bin\checkver.ps1 allure -u
scoop update allure
```

### Mac OS X

```brew
brew install allure
```

### 检查是否安装成功

```bash
allure --version
```

## 关键特性

* `feature`: 用于定义被测试的功能，被测产品的需求点
* `story`: 用于定义被测功能的用户场景，即子功能点
* `step`: 用于将一个测试用例，分成几个步骤在报告中输出
* `attach`: 用于向测试报告中输入一些附加的信息，通常是一些测试数据信息

## 运行

## 工程集成

### Java

### Javascript

