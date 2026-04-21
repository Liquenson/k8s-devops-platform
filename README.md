# 🚀 k8s-devops-platform

> Plataforma GitOps para despliegue continuo en Kubernetes usando ArgoCD como controlador declarativo

[![Kubernetes](https://img.shields.io/badge/Kubernetes-1.29-326CE5?logo=kubernetes)](https://kubernetes.io/)
[![ArgoCD](https://img.shields.io/badge/ArgoCD-GitOps-EF7B4D?logo=argo)](https://argo-cd.readthedocs.io/)
[![Docker](https://img.shields.io/badge/Docker-Containers-2496ED?logo=docker)](https://www.docker.com/)
[![GitOps](https://img.shields.io/badge/GitOps-Declarative-blue)](https://opengitops.dev/)

**k8s-devops-platform** implementa una arquitectura moderna basada en **GitOps**, donde Kubernetes se gestiona de forma completamente declarativa y automatizada mediante ArgoCD.

**En resumen:** despliegues automáticos en Kubernetes sin intervención manual, usando Git como única fuente de verdad.

---

## ⚡ Arquitectura

GitHub (Source of Truth)
↓
ArgoCD (Continuous Delivery Controller)
↓
Kubernetes Cluster
↓
Aplicaciones (NGINX)

**Componentes principales:**

* ✅ **GitHub** como fuente única de configuración
* ✅ **ArgoCD** para sincronización automática
* ✅ **Kubernetes** como plataforma de ejecución
* ✅ **Manifiestos declarativos** versionados
* ✅ **Aplicación NGINX** como ejemplo funcional

---

## 🚀 Inicio Rápido

### Requisitos

```bash
- Kubernetes cluster (local o cloud)
- kubectl
- ArgoCD instalado
- Git
```

### Despliegue en 4 pasos

```bash
# 1. Clonar repositorio
git clone https://github.com/Liquenson/k8s-devops-platform.git
cd k8s-devops-platform

# 2. Crear namespace de ArgoCD (si no existe)
kubectl create namespace argocd

# 3. Acceder a ArgoCD (UI o CLI)
# Configurar conexión al repo

# 4. Sincronizar aplicación
# ArgoCD desplegará automáticamente nginx
```

---

## 📊 Stack Tecnológico

### Plataforma

| Componente | Uso                          |
| ---------- | ---------------------------- |
| Kubernetes | Orquestación de contenedores |
| ArgoCD     | GitOps / Continuous Delivery |
| Docker     | Contenedores                 |

### DevOps

| Herramienta | Uso                 |
| ----------- | ------------------- |
| GitHub      | Source of Truth     |
| Git         | Versionado          |
| kubectl     | Gestión del clúster |

---

## 🏗️ Estructura del Proyecto

```bash
k8s-devops-platform/
├── apps/
│   └── nginx/
│       ├── deployment.yaml     # Deployment (2 réplicas)
│       └── service.yaml        # Servicio NodePort
│
├── clusters/
│   └── local/                  # Configuración de entorno
│
└── README.md
```

---

## 🔄 Flujo GitOps

Git Push
↓
ArgoCD detecta cambios
↓
Sincronización automática
↓
Kubernetes aplica estado deseado

**Resultado:**

* ❌ Sin `kubectl apply`
* ✅ Despliegue automático
* ✅ Estado consistente
* ✅ Auditoría completa vía Git

---

## 📱 Aplicación Desplegada

### NGINX (Demo)

* 2 réplicas en ejecución
* Servicio tipo NodePort
* Gestionado 100% por ArgoCD

---

## 🔒 Seguridad

### Implementado

✅ Control declarativo (sin cambios manuales)
✅ Histórico en Git (auditoría completa)
✅ Separación de responsabilidades
✅ Rollback automático vía Git

### Buenas prácticas recomendadas

* Uso de RBAC en Kubernetes
* Integración con secrets manager
* Restricción de acceso a ArgoCD
* Uso de namespaces por entorno

---

## 📈 Casos de Uso

### Para DevOps Engineers

```bash
# Implementar GitOps real
# Automatizar despliegues
# Eliminar configuración manual
# Controlar estado del cluster
```

### Para Equipos de Desarrollo

```bash
# Deploy automático con git push
# Entornos reproducibles
# Versionado de infraestructura
# Menos dependencia de operaciones
```

### Para Arquitectos Cloud

```bash
# Arquitectura declarativa
# Alta trazabilidad
# Integración con CI/CD
# Escalabilidad en Kubernetes
```

---

## 📖 Verificación

```bash
kubectl get pods
kubectl get svc
```

---

## 🎯 Conceptos Demostrados

* GitOps
* Continuous Delivery
* Infraestructura declarativa
* Kubernetes deployments
* Automatización de despliegues

---

## 🚀 Roadmap

### v1.0.0 (Actual)

* ✅ GitOps básico con ArgoCD
* ✅ Despliegue NGINX
* ✅ Estructura de repositorio

### v1.1.0 (Próximo)

* 🚧 Auto-sync habilitado
* 🚧 Multi-entorno (dev/staging/prod)
* 🚧 Integración Helm/Kustomize

### v2.0.0 (Futuro)

* 🔮 CI/CD completo (GitHub Actions)
* 🔮 Integración con monitoring
* 🔮 Ingress + dominio
* 🔮 Seguridad avanzada (RBAC + secrets)

---

## 👨‍💻 Autor

**Liquenson Ruben Alexis**
*DevOps Engineer | Cloud Engineer | Linux System Administrator | AWS | Kubernetes*

* 📧 [liquenson.cloud@gmail.com](mailto:liquenson.cloud@gmail.com)
* 💼 LinkedIn: https://www.linkedin.com/in/liquenson-ruben-490961269/
* 🐙 GitHub: https://github.com/Liquenson
* 📍 Las Palmas de Gran Canaria, España

---

## 📄 Licencia

MIT License - Ver [LICENSE](LICENSE)

---

## 🔗 Proyectos Relacionados

* aws-terraform-devops-lab → Infraestructura AWS con Terraform
* linux-fleet-manager → Automatización Bash de servidores

---

⭐ **¿Te resulta útil? ¡Dale una estrella!**

**¿Preguntas?** Abre un issue o contáctame por email.
