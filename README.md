## Estructura del Proyecto
Este repositorio gobierna la configuración de los elementos del clúster mediante el repositorio de aks-gitops-cluster-configuracion en donde se encuentra las configuraciones post aprovisionamiento y configuración del addons de gitops.
```bash
.
└── infrastructure
    ├── base
    │   └── ingress-nginx
    │       ├── kustomization.yaml
    │       └── namespace.yaml
    └── dev
        └── ingress-nginx
            ├── helmrelease.yaml
            └── helmrepository.yaml
```

## Descripción de Archivos y Directorios

**infrastructure/base:** Contiene las configuraciones base que incluyen el namespace requerido para el Ingress controller.

| **ingress-nginx/kustomization.yaml:** Define los recursos que se aplicarán, en este caso, el namespace.

| **ingress-nginx/namespace.yaml:** Manifiesto para crear el namespace ingress-nginx.

| **ingress-nginx/helmrepository.yaml:** Define el repositorio de Helm para NGINX.

| **ingress-nginx/helmrelease.yaml**: Describe el despliegue del Ingress controller usando helm.