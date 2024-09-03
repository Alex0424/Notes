# Cloud Service Models

Different models depending on what we're buying from the cloud provider. Each has its own pros and cons.

From the top-down:
- FaaS: Function as a service
- CaaS: Container as a service
- SaaS: Software as a service
- PaaS: Platform as a service
- IaaS: Infrastructure as a service

![image](https://github.com/user-attachments/assets/0141b1b7-3398-4a50-9586-0c37901319da)

## IaaS

Infrastructure As A Service.

Provisioning of: machines, network, storage.

Access to machines/VM in a datacenter.
- Choice of virtual resources (vCPU & RAM)
- Pluggable storage solutions
- Could be VM or bare metal(dedicated server)
- - not as common as VMs

Control over your infrastructure

Can buy extra resources as-needed
- CapEx becomes OpEx
 
Possibility to automate and scale

Features vary between providers

Avoid lock-in by using FOSS solutions
- keep migration a possibility w/help of well-documented processes
- Example: OpenStack

## PaaS 

Plattform As A Service

Readymade system to deploy your code/application in
- Perfect for DevOps playground

i.e.: The platform deploys your code and runs it(possibly in a container)

the platform is managed by the provider

removes the responsibility for the hardware and underlying system from your practices

How to know what CVEs are relevant?

Avoid lock-in

Examples: Jelastic, OpenShift, CloudFoundry, Google apps

## SaaS

Software As A Service

