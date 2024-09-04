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

Cloud based applications delivered to users.

Ready enviroment with installed application(s)

The provider is responsible for the maintenance and updates, all the way from the application...
- ...to the metal, including all layers in-between*.

"Easy" GUI used for configuring (harder when more configurations)

Easy to scale, probably license-driven

Make life easy for your IT-department

*Note: different providers could be responsible for different layers, i.e.: provider X sells you a license for a SaaS product they maintain on a PaaS platform provided by Provider Y that runs on Provider Z's metal(IaaS)

Data security
- not in your control

Lock-in?

You might need to adapt your processes to the tool, and not the other way around(i.e. the product won't be tailored after your needs)

Integrations
- are they possible?
- do they require a higher tier license?
- will they be maintained in the future(looking at you, Slack)
- "You have no power here"

Performance
- outside your control

Example: GSuit, Nextcloud, Dropbox, Slack, Trello, Salesforce.

## CaaS

Container As A Service


You buy access to a container orchestrator
- start & stop containers
- scale (scale horizontal and vertical)
- shedule
- manage containers

CaaS managed
- the provider takes responsibility for the underlying infrastructure(i.e.: Kubernetes cluster) 
- the provider takes care of everything except your containers

Prtability
- if your container works, you can deploy it anywhere else

Resource effective(compared to VMs/bare metal)

isolation - each container is independent

Easily scalable - spin up another one & load balance
- possibility to scale horizontally

Fault tolerant - spin up more...

Example: kubernetes cluster

FaaS

Function As A service

Even finer granularity

"Run my code, only when needed"

Pay only for CPU cycles used - only when the function is executed
- Reduce overhead
- Pro - extremely effective use of OpEx
- - Completely managed by the provider
  - the least amount of moving parts to care about
- Cons - almost guaranteed lock in
- - completely dependent of your provider's APIs, you write your code based on your FaaS provider
  - completely managed by provider

![image](https://github.com/user-attachments/assets/24b1a890-7168-4868-ade7-c48e7e040926)

# Economy

### Why do i need to know anything about economy?

To more easily get your voice heard in the organization
- the people who takes the decisions in an organization...
- ...are usually responsible for a budget for a certain team/project.

The other side: how much IT-knowledge is expected of the people responsible for budgets?
- A little jargon/lingo goes a long way.
- If you speak their language, they can more easily uderstand you.

Example: you're trying to convince your boss to not go in a certain direction (related to the technological aspect of your team's work). It might be more fruitful to bring forward an economic reason why the decision should be made according to your opinion, along with technical reasons.






















42:40
