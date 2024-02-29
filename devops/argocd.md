# ArgoCD

## Installation

Source: https://argo-cd.readthedocs.io/en/stable/getting_started/

```
kubectl create namespace argocd
kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml
```

### Access the Web UI at https://localhost:8080

```
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

username is `admin` and password can be retrived with `kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d`

### CLI

Source: https://argo-cd.readthedocs.io/en/stable/cli_installation/

```
https://argo-cd.readthedocs.io/en/stable/cli_installation/
```
