# OpenStack

OpenStack is a cloud plattform that can hadle large pools of VM and container instances, storageand network resources in one or more datacenters.

It's managed via GUI or CLI

Delivers Infrastructure as a Service (IaaS) and more.

- Elasticity
- Virtualization
- Orchestration

Components:

- Nova (Instances)
- Neutron (networking)
- Cinder (block storage)
- Swift (object storage)
- Manilla (Shared File System)
- Glance (OS images)
- Horizon (dashboard)
- Skyline (newer dashboard)
- Octavia (load balancer)
- Barbican (secrets management)
- Keystone (identity management)
- Heat (orchestration)
- Ceilometer (Telemetry/Collects data on resource usage for billing and benchmarking)
- Aodh (Alarming and notification based on metrics)
- Sahara (Data processing)
- Ironic (Bare Metal Provisioning)

There are 33 distinct components in OpenStack

# Nova

Implements and manages services and libraries needed to manage scalable, on-demand, self-serviced access to compute resources, including virtual machines and containers.

### Nova components

- Nova-api: talks to the clients
- Nova-compute: creates and terminates VMs
- Nova-volume: volume management for instances
- Nova-network: manages network for instances
- Nova-sheduler: manages which hardware a VM is sheduled on
- - The VM is sheduled in a 2-step process, where the available hardware is first filtered and then prioritized against each other for example:
- - simple: host with least load
- - random: self-explanatory
- - zone: random host in a given AZ
- - other choices filtered on: RAM, CPU, storage, etc...

#### Nova Flavours

this is up to the provider

| Flavour        | CPU | RAM    | STORAGE    |
----------------------------------------------
| v1-micro-1     | 1   | 0.5 GB | 20 GB SSD  |
----------------------------------------------
| v1-standard-1  | 1   | 4 GB   | 40 GB SSD  |
----------------------------------------------
| v1-standard-4  | 4   | 16 GB  | 160 GB SSD |
----------------------------------------------
| v1-dedicated-8 | 8   | 64 GB  | 800 GB SSD |
----------------------------------------------

# Neutron

OpenStack Neutron is an SDN networking project focused on delivering networking-as-a-service (NaaS) in virtual compute enviroments.

# Cinder

Cinder is a Block Storage service for OpenStack. It virtualizes the monagement of block storage devices and provides end users with a self service API to request and consume those resources without requiring any knowledge of where their storage is actually deployed or on what type of device.

# Swift

Swift is a highly available, distributed, eventually consistent object/blob storage.

# Glance

iso images

# Horizon

dashboard over all available oponents and a view over our infrastructure

# Skyline

also dashboard but newer and probobly faster

# Octavia 

Loadbalancer 

Octavia runs on dedicated instances

based on HAProxy

Redundant, active/passive

TLS

several services per LB

stores certificates in Barbican

# Barbican

Barbican is the OpenStack Key Manager service.

It provides secure storage, provisioning and management of secret data, such as passwords, encryption keys, X.509 Certificates and raw binary data.

# Keystone

Ketstone is an OpenStack service that provides API client authentication, service discovery, and distributed multi-tenant autorization by implementing OpenStack's identity API.

It supports LDAP, OAuth, OpenID Connect, SAML and SQL.

# Heat

Heat orchestrates the infrastructure resources for a cloud application based on templates in the form of text files that can be treated like code

Heat provides both an OpenStack-native RsST API and a CloudFormation-compatible Query API.

Heat also provides an autoscaling service that integrates with the OpenStack Telemetry services, so you can include a scaling group as a resource in a template.

# Links for INFO About OpenStack

https://www.openstack.org/software/project-navigator/openstack-components#openstack-services
