# Cloud template project

Template project that is focused on providing know-how on how to setup CI/CD anywhere based on kubernetes.

## Step 1

[Deploy cluster](https://docs.k0sproject.io/v1.28.4+k0s.0/k0sctl-install/#3-deploy-the-cluster):

`k0sctl apply --config k0s/k0sctl.yaml`

Export kubeconfig:

`k0sctl kubeconfig --config k0s/k0sctl.yaml > cloud-kube-config`

Destroy cluster:

`k0sctl reset --config k0s/k0sctl.yaml`
