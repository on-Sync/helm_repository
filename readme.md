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

# Install

```bash

# Open source

> helm install {release} -f values/{value.yaml} {repo}/{chart}

# My Application

> helm install {release} {my_chart}

```