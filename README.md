## Alertmanager概述

- Alertmanager与Prometheus是相互分离的两个部分。
- Alertmanager处理由例如Prometheus服务器等客户端发来的警报。
- Alertmanager负责删除重复数据 , 分组，并将警报通过路由发送到正确的接收器，比如Email、Slack等

## Install
1. 创建`alertmanager configmap`
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/Alertmanager/master/alertmanager-configmap.yaml
```

2. 部署`alertmanager`服务
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/alertmanager/master/alertmanager-deployment.yaml
```

3. 部署`alertmanager ingress`服务
```sh
kubectl apply -f https://raw.githubusercontent.com/Donyintao/alertmanager/master/alertmanager-ingress.yaml
```
