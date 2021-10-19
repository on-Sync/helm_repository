# Helm `21-10-19`

## Reference Repository

```bash
> helm repo list

NAME            URL
bitnami         https://charts.bitnami.com/bitnami
=> rabbitmq
ingress-nginx   https://kubernetes.github.io/ingress-nginx
jenkins         https://charts.jenkins.io
```

## Network

```bash
# `Web server` 로 `ingress-nginx` 를 활용합니다.
kubernetes.io/ingress.class: nginx

# `Package` 단위로 `Host`를 공유합니다.
jenkins.local
config-server.local
...

# `Component` 단위는 `Nginx`의 `Rewrite` 사용합니다.
nginx.ingress.kubernetes.io/rewrite-target: /$2
path: config-store(/|$)(.*)
```