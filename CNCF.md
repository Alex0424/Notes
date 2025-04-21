# 🌩️ Cloud Native Computing Foundation (CNCF)

CNCF is an open-source software foundation that hosts and nurtures projects like **Kubernetes** and **Prometheus**.

- 🚀 Fosters the evolution of projects and the entire ecosystem  
- 🔄 Always up to date  
- ✅ Ensures good compatibility  
- 🌱 Promotes success for the entire ecosystem  

### 🌐 Cloud Native Landscape / Ecosystem (Open Source)

- Landscape Example: https://landscape.cncf.io  
- Encompasses all the categories, projects, and companies  
- Over **450** cards in this ecosystem  

👉 It's recommended to visit the **Trailmap for Beginners**: https://github.com/cncf/trailmap

---

# ⚙️ Management and Orchestration

1. **Containerize your application** (e.g., Docker, Containerd, Podman)  
2. **Continuous Integration**  
   - Build container image  
   - Store it in an image repository  
   - ✅ Use **Argo** for CI/CD  
3. **Continuous Delivery**  
   - Deploy to staging or production environments  

### 🚀 How to run containers?

Use **Kubernetes**: https://kubernetes.io/docs/tutorials/kubernetes-basics/

- Run containers at scale  
- Efficiently manage compute resources  
- Cloud-agnostic  
- Great for simple applications (via Kubernetes manifests)  
- For complex microservices, use a package manager like **Helm**  
  - Helm: https://helm.sh  
    - Define, install, and upgrade Kubernetes apps with **Helm Charts**  
    - Create, version, share, and publish Helm Charts  
    - 🧰 Think of it like `apt` for Linux or `npm` for JavaScript  

### 🔁 Alternate Paradigms (CNCF Projects for Communication)

- HTTP APIs: REST, SOAP  
- Remote Procedure Calls: **gRPC** (better if REST or SOAP performance is lacking)  
- Messaging/Queuing: **NATS**  
- Eventing: **CloudEvents**

---

## 🔎 Service Discovery

**Tools**: Consul, etcd, CoreDNS  
- Kubernetes uses **etcd** as its primary data store  
- Kubernetes uses a DNS provider like **CoreDNS**  

### CoreDNS

- 🎓 CNCF Graduated Project  
- Fast & Flexible  
- Plug-in architecture  
- Written in **Go** – extensible via plugins  
- ✅ Recommended for Kubernetes

---

## 📦 Container Registry

A container registry is a place to store and share container images.

You can **push** images to a registry and **pull** them into environments like Kubernetes clusters.

### Popular Container Registries:

- Docker Hub  
- GitLab  
- JFrog  
- Harbor  
- Cloud Provider Registries (e.g., Azure Container Registry)

### CNCF Registry: **Harbor**

- 🔓 Open-source registry  
- Secures artifacts with policies & RBAC  
- Scans images for vulnerabilities  
- Supports trusted image signing  
- 🎯 Great choice if your company doesn’t already have a registry  
- 🎓 CNCF Graduated Project

---

## 📈 Managing Cloud-Native Services

👤 *Karthik Gaekwad* predicts **Service Management** will grow rapidly in the coming years.

- The goal: create tools that deploy and manage apps effectively  
- **Kubernetes** solves this problem elegantly  

### Dev & Ops Needs:

- **Ops**: "How do I scale nodes?"  
- **Dev**: "How can I manage apps better?"  

These are addressed in the **Service Management** architecture.

---

## 🔗 Service Mesh

Handles communication and network intricacies between microservices.

### 🔹 Linkerd

- Transparent network proxy  
- Provides service mesh capabilities  
- One-stop for managing, controlling, and monitoring service-to-service communication  
- 🌍 Widely used globally  
- Makes code scalable, performant, and resilient  

**Features:**
- Latency-aware load balancing  
- Connection pooling  
- TLS (Transport Layer Security)  
- Instrumentation

### 🔹 Envoy

- Originated from Linkerd  
- Written in C++  
- Small server with minimal footprint  
- Supports HTTP/2 and gRPC  
- Advanced load balancing: rate limiting, retries, etc.  
- Request-level routing  
- Highly configurable with APIs  
- Allows distributed tracing and observability at the wire level

### 🔍 Key Differences

**Linkerd:**
- Heavier: consumes more CPU and memory  
- Minimalistic configuration  
- Hot reloads supported natively  
- Supports service abstraction and dynamic provisioning  
- Protocol support: Thrift, HTTP/2, gRPC  

Both are great for REST-style microservices.

---

# 🌐 Networking and Runtime

### Container-Native Networking (in CNCF Landscape)

🔌 Can be confusing at first – focus on **CNI**!

### CNI – Container Network Interface  
GitHub: https://github.com/containernetworking/cni

1. Plugin-based networking solution  
2. Container runtime decides network and plugins  
3. Runtime adds container to each network sequentially using plugins  
4. Network config is a **JSON file**

🧠 The container runtime must create a new **network namespace** for each container.

### Popular Networking Providers for Kubernetes:

- **Project Calico**  
- **Flannel**

### Database Storage

more info coming soon, taking a break for now.
\\1 before 4.Application Observability...

# Application Observability, Analysis, and Security

  
