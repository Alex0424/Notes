# Cloud Native Comouting Foundation

CNCF is an open source software foundation that hosts and nurtures projects like Kubernetes and Prometheus.

- It fosters the evolution of project and the entire ecosystem
- Always up to date
- Good compatibility
- promotes success for entire eco-system

# Cloud Native Landskape/Ecosystem (Open Source)

## website example: https://landskape.cncf.io

- Encompasses all the categories, projects and companies.
- Over 450 cards in this ecosystem.

# Its recomended to visit trailmap for begginers: https://github.com/cncf/trailmap

1. Containerize your application (Docker, ContainerD, Podman)
2. Continue Integration (Build container image, Store in image repository) [use argo for cicd]
3. Continous delivery (Deploy staging or production enviroment)
4. How to run container?
   - With Kubernetes:
     - Allows you to run your containers at scale.
     - Manages compute resources elegantly.
     - Cloud agnostic.
     - Kubernetes manifest good for simple application.
     - But needs a package manager for complex microservices.
       - Popular choice is Helm: https://helm.sh.
         - It allows you to define, install, and upgrade Kubernetes applications via Helm Charts.
         - You can create, version, share and publish Helm Charts.
         - Think of it like apt for linux, NPM for node/javascript application.
    - Alternate Paradigms:
      - HTTP APIs: REST or SOAP
      - 
