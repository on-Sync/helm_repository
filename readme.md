# Helm `21-10-19`

## Repo List

```bash
> helm repo list

NAME            URL
bitnami         https://charts.bitnami.com/bitnami
eks             https://aws.github.io/eks-charts
cloudposse      https://charts.cloudposse.com/incubator/
ingress-nginx   https://kubernetes.github.io/ingress-nginx
stable          https://charts.helm.sh/stable
jenkins         https://charts.jenkins.io
```

## Install

```bash

# Open source

> helm install {release} -f values/{value.yaml} {repo}/{chart}

# My Application

> helm install {release} {my_chart}

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