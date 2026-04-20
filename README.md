# 🚀 k8s-devops-platform

Plataforma de despliegue basada en **GitOps** utilizando Kubernetes y ArgoCD.

---

## 📌 Descripción

Este proyecto implementa un flujo moderno de DevOps donde las aplicaciones se despliegan y gestionan mediante **principios GitOps**.

Todos los recursos de Kubernetes están definidos de forma declarativa en Git, y **ArgoCD se encarga de sincronizar automáticamente el estado del clúster con el estado deseado**.

---

## 🧠 Arquitectura

```text
GitHub (Source of Truth)
        ↓
     ArgoCD
        ↓
   Kubernetes Cluster
        ↓
     Aplicación (NGINX)
```

---

## 📂 Estructura del proyecto

```bash
k8s-devops-platform/
├── apps/
│   └── nginx/
│       ├── deployment.yaml
│       └── service.yaml
├── clusters/
│   └── local/
└── README.md
```

---

## ⚙️ ¿Cómo funciona?

1. Los manifiestos de Kubernetes se almacenan en Git
2. ArgoCD monitoriza el repositorio
3. Detecta cambios automáticamente
4. Sincroniza el clúster con el estado definido

👉 No es necesario usar `kubectl apply` manualmente

---

## 🚀 Aplicación desplegada

### 🔹 NGINX (Aplicación de ejemplo)

* 2 réplicas en ejecución en Kubernetes
* Expuesta mediante un servicio NodePort
* Gestionada completamente con ArgoCD

---

## 🔄 Flujo GitOps

```text
git push → ArgoCD → Kubernetes
```

---

## 🛠️ Tecnologías utilizadas

* Kubernetes
* ArgoCD
* Docker
* GitHub

---

## 📊 Verificación

```bash
kubectl get pods
kubectl get svc
```

---

## 🎯 Conceptos demostrados

* GitOps
* Infraestructura declarativa
* Continuous Delivery
* Gestión de recursos en Kubernetes

---

## 🚀 Mejoras futuras

* Activar Auto-Sync (CD real)
* Separación de entornos (dev/staging/prod)
* Integración con Helm o Kustomize
* Pipeline CI/CD con GitHub Actions
* Configuración de Ingress

---

## 👨‍💻 Autor

Liquenson Ruben
DevOps Engineer | Cloud Engineer | Linux System Administrator | AWS | Kubernetes

