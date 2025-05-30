# Blog App con Kubernetes, DockerHub y ArgoCD

## Descripción
Este proyecto consiste en una aplicación Flask desplegada en un clúster de Kubernetes usando Minikube. La gestión del despliegue se realiza con ArgoCD y la imagen de la app se almacena en DockerHub.

## Pasos realizados

1. **Construcción y subida de la imagen Docker**
   - Se creó un `Dockerfile` para la app Flask.
   - Se construyó la imagen y se subió a DockerHub bajo el usuario `alejandromons`.

2. **Manifiestos de Kubernetes**
   - Se crearon manifiestos en la carpeta `k8s` para el Deployment y Service de la app.
   - El Deployment usa la imagen de DockerHub y expone el puerto 5000.
   - El Service expone la app como NodePort.

3. **Despliegue con ArgoCD**
   - Se instaló ArgoCD en el clúster Minikube.
   - Se creó una aplicación en ArgoCD que referencia el repositorio de GitHub y la carpeta `k8s`.
   - Se verificó el estado de la app desde la interfaz web de ArgoCD.

4. **Verificación**
   - Se comprobó que la app está corriendo en el clúster con `kubectl get pods`.
   - Se accedió a la app desde el navegador usando la URL proporcionada por Minikube.

## Evidencias
- Pantallazos de la interfaz de ArgoCD mostrando la app creada y en estado Healthy.
- Pantallazos de la app corriendo en el navegador y del pod en estado Running.

## Autor
Alejandro Monsalve 