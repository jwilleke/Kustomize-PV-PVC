# Demo of Kustomize PV PVC

## Preop work

On host running Kuberneties Cluster

``` bash
mkdir -p /mnt/data-pv/
nano /mnt/data-pv/index.html

# enter some thing like <h1>Hello from kustomize-pv-pvc persistent volume</h1>
```

## Create Kustomize Folder Structure

Soemthing like:

```kustomize-pv-pvc/
├── base/
│   ├── pv.yaml
│   ├── pvc.yaml
│   └── deployment.yaml
|   |__ service.yaml
├── overlays/
│   └── kustomization.yaml
└── kustomization.yaml
└── namespace.yaml
```
