# Demo of Kustomize PV PVC

## Prep work

On host running Kuberneties Cluster

``` bash
mkdir -p /mnt/appsdata/nginx-app/
nano /mnt/appsdata/nginx-app/index.html
# enter some thing like <h1>Hello from kustomize-pv-pvc persistent volume</h1>
```

Editing ```/mnt/appsdata/nginx-app/index.html``` will cause updates to the file after a refressh of page.


## Create Kustomize Folder Structure

Soemthing like:

```
hostname/apps/k8s/apps
|- nginx-app-demo/
├── base/
│   ├── pv.yaml
│   ├── pvc.yaml --> Not used see volumeClaimTemplates in statefulset.yaml
│   |__ statefulset.yaml
|   |__ service.yaml
|   |__ nginx-app-ingress.yaml
├── overlays/
│   └── kustomization.yaml
└── kustomization.yaml
└── namespace.yaml
```


!! status 

<http://nginx-app.nerdsbythehour.com/> WORKS