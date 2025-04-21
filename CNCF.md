# Cloud Native Comouting Foundation

CNCF is an open source software foundation that hosts and nurtures projects like Kubernetes and Prometheus.

- It fosters the evolution of project and the entire ecosystem
- Always up to date
- Good compatibility
- promotes success for entire eco-system

- Cloud Native Landskape/Ecosystem (Open Source)

- Landskape example: https://landskape.cncf.io

- Encompasses all the categories, projects and companies.
- Over 450 cards in this ecosystem.

Its recomended to visit trailmap for begginers: https://github.com/cncf/trailmap

# Management and Orchestration

1. Containerize your application (Docker, ContainerD, Podman)
2. Continuos integration (Build container image, Store in image repository) [use argo for cicd]
3. Continuos delivery (Deploy staging or production enviroment)
4. How to run container?
   - With Kubernetes(https://kubernetes.io/docs/tutorials/kubernetes-basics/):
     - Allows you to run your containers at scale.
     - Manages compute resources elegantly.
     - Cloud agnostic.
     - Kubernetes manifest good for simple application.
     - But needs a package manager for complex microservices.
       - Popular choice is Helm: https://helm.sh.
         - It allows you to define, install, and upgrade Kubernetes applications via Helm Charts.
         - You can create, version, share and publish Helm Charts.
         - Think of it like apt for linux, NPM for node/javascript application.
    - Alternate Paradigms(Stream data, messaging interface for microservices) CNCF projects example:
      - HTTP APIs: REST or SOAP
      - Remote procedure calls: gRPC (good choice if REST or SOAP arent performant well)
      - Messaging or queuing: NATS
      - Events: cloud events

### Service discovery

Tools: Consul, etcd, CoreDNS
- kubernetes have etcd cluster to store its data.
- kubernetes have a DNS(e.g.: CoreDNS) provider for the DNS layer.

CoreDNS:
- CNCF graduated project
- Fast and flexible
- Plug-in architecture
- Written in Golang: so if a func is not out of the box, you can add to it by writing a plugin.
- recomended for kubernetes

### Container Registry
- A container registry essentially acts as a place for developers to store container images and share them out via a process of uploading (pushing) to the registry and downloading (pulling) into another system, like aKubernetes cluster. Once you pull the image, the application within it can be run on that system.
- Container registry hosts:
- Docker Hub
- Gitlab
- Jfrog
- Harbor
- Cloud providers have container registry as well e.g.: Azure
- CNCF Container Registry: Harbor:
  - Open-source registry that secures artifacts with policies and role-based access control.
  - It ensures that images are scaned and free from vulnerabilities and signs images as trusted (Good choice if company dont have a registry allready).
  - It looks full featured and is a graduated CNCF project.

### Managing cloud native services

Karthik Gaekwad estimates that Service Management will show most growth in the next few years.

Goal was to create an "Operation tool" that can deploy and manage your application.
- This is where cubernetes comes in and solves the problem in an elegant fashion.
- As Kubernetes grew many people asked about OPS(How do i scalable nodes) and DEV(How can i manage application in a better way?)
- - This is captured in Service Management diagram.

### Service Mesh

The layer that handles all of the communication and network intricacies between microservices.

- Linkerd
  - Transparent network proxy
  - Acts as a service mesh
  - One-stop shop for managing, controlling, and monitoring service-to-service communication in large application
  - Used extensively around the world.
  - Use this to simplify communication within their software inrastructure.
  - Features include
    - latancy-aware load balancing
    - connection pooling
    - Transport Layer Security(TLS)
    - Instrumentation
    - This makes your code scalable, performant and resiliant

Envoy
- comes from Linkerd and was written in C++
- Idea of Envoy is similar to Linkerd
- Small server with small footprint
- supports http2 and gRCP
- Supports advanced load balancing e.g.: rate limiting, automatic retries...
- request-level routing 
- Highly configurable, providing APIs for configuration management.
- Allows distributed request tracing and wire-level observabillity.

### Differences?
Linkerd
- bigger consumes more cpu and memmory, offers minimalistic configuration
- business support hot reloads by design.
- instead relying on service abstractions and dynamic provisioning.
- Support the Thrift protocol in addition http2 and gRCP. 

Envoy and Linkerd are simple for REST-style services.

# Networking and Runtime

### Container native networks.

# Application Observability, Analysis, and Security

  
