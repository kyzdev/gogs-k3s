# gogs-k3s

A kubectl YAML to deploy GOGS on Kubernetes

## Post-Installation

You can tune the prod or dev Kustomize Overlay with :
- gogs-deployment.yaml : to match your storage driver (in my example I use a NFS driver),
- gogs-ingressroute.yaml : to match your FQDN.

## Installation 

```bash
git clone https://github.com/kyzdev/gogs-k3s
cd gogs-k3s
kubectl apply -k overlays/prod
```
## Uninstallation

```bash
kubectl delete namespace prod-gogs
```