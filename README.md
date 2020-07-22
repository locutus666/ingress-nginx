## 1. 准备

- 下载配置文件到本地

```bash
# git clone https://github.com/locutus666/ingress-nginx.git
```

- 在选取的ingress-nginx节点，下载ingres-nginx镜像

```bash
# docker pull locutus1/ingress-nginx:v0.34.1

# docker tag locutus1/ingress-nginx:v0.34.1 k8s.gcr.io/k8s-artifacts-prod/ingress-nginx/controller:v0.34.1
```

- 给选取的ingress-nginx节点打标签

```bash
# kubectl label nodes node01 ingress-nginx-controller-0.34.1=true
```

<br/>

## 2. 升级ingress-nginx

- 部署yaml文件

```bash
# kubectl apply -f .
```

- 验证pod正常启动

```bash
# kubectl get pod -n ingress-nginx
```

<br/>

## 3. 验证外部网络访问

在浏览器中，访问应用域名，检查是否正常。
