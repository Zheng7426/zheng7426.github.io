---
category: DevOps
title: K8s 使用笔记
author: Hz.
---

[Setup](#Setup)

## Setup
我们可以借助一些工具方便在本地探索 Kubernetes 的功能。

首先下载两个软件:
- _Docker Desktop_
- _Minikube_

满足以上环境条件之后，启动 Docker Desktop。

然后打开控制台，执行 `minikube start`。

```bash
🏄  Done! kubectl is now configured to use "minikube" cluster
and "default" namespace by default
```

在成功启动 minikube 之后，控制台显示 kubectl 现在使用 "minikube" 集群，并且默认的命名空间是 "default"。

kubectl 是 k8s 主要的命令行工具，我们安装 Minikube 的同时也会自动装上 kubectl，该工具的配置文件通常位于当前用户根目录(～)的 .kube 文件夹下。

我们通过 `cat $HOME/.kube/config` 或者 `kubectl config view` 命令可以查看配置文件的内容。

```config
apiVersion: v1
clusters:
- cluster:
    certificate-authority: ...
    server: https://127.0.0.1:53352
  name: minikube
contexts:
- context:
    cluster: minikube
    namespace: default
    user: minikube
  name: minikube
current-context: minikube
kind: Config
preferences: {}
users:
- name: minikube
  user:
    client-certificate: /Users/.../.minikube/profiles/minikube/client.crt
    client-key: /Users/.../.minikube/profiles/minikube/client.key
```

配置文件中有以下 3 个定义我们可以注意一下:
- _Clusters_
- _Contexts_
- _Users_

`kubectl config current-context`


## Example Project
我们先去生成一个测试用的项目，目的是将其容器化，且用 k8s 来对容器进行编排。

使用 Spring initializer 生成一个 Java 后端项目。


## Dockerfile
## Pod
## Deployment
## Service 
## Storage
## ConfigMap

