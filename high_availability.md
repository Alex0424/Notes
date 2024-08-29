# High Availability
31.45

High availability(HA) is a characteristic of a system which aims to ensure an agreed level of operational performance, usually uptime, for a higher than normal period.

#### To achive HA
- Service Level Agreement (SLA)
- Service Level Objective (SLO)
- Downtime
- Uptime
- Maintenance/Service window
- Fault tolerance
- Redundancy
- Scalability
- Elasticity

#### What if something DOES go wrong?
- Backup
- Restore
- RPO
- RTO
- Business Continuity/Disaster Recovery play

#### SLAs, SLOs, Measurements & The Graph
- in comercial context, you are obliged to deliver based on SLAs and SLOs.
- To determine if you did it, measurements and reports are needed.

#### SLA?
- A service-level agreement(SLA) is a commitment between a service provider and a aclient.
- Particular aspects of the service - quality, availability, responsibilities - are agreed between the service provider and the service user.
- The most common component of an SLA is that the service should be provided to the customer as agreed upon the contract.
- The service level objective(SLOs) are a part of SLA.

#### Example components of an SLA
- ISPs & telcos will commonly include SLAs within the terms of their contracts with customers to define the levels of service being sold.
- SLA will have a technical definitions such as:
  - Mean time between failures(MTBF)
  - Mean time to repair or mean time to recover(MTTR)
  - Uptime(per year, for instance 99.999%, or "five nines")
  - identifying wich part is responsible for reporting faults or paying fees.
  - Responsibility for data rates, throughput, jitter or similar measurable details
  

### SLO

SLOs must be:
- attainable
- repeatable
- measurable
- understandable
- meaningful
- controllable
- affordable
- mutually acceptable

Examples of SLOs
- Availability: `The application will be available 99.95% of the time`
- Over a year
- Service Desk Response
  - 75% of help desk calls will be answered in less than a minute
  - 85% of help desk calls will be answered within two minutes
  - 100% of help desk call will be answered within three minutes
- Over a month

- Incident Response Time
  - 99% of severity 1 tickets will be resolved within 3hrs
  - 98% of severity 2 tickets will be resolved within 8hrs
  - 98% of severity 3 tickets will be resolved within 3 business days
  - 98% of severity 4 tickets will be resolved within 5 business days
- Over a quarter

Responce Time
- 85% of TCP replies within 1.5 seconds of receiving a request
- 99.5% of TCP replies within 4 seconds of receiving a request
Over a month

Measurements & The Graph

Many ways to measure SLAs and SLOs
- Logs, pings, 3rd party sites, customer experience, customer ratings, etc...
- Logging you all know by heart

#### Grafana
As a visualization tool, Grafana is a popular component in monitoring stacks

It is often used in combination with time series databases such as InfluxDB, Prometheus and Graphite.

or in combination with monitoring platforms such as Sensu, Icinga, Checkmk, Zabbix, Netdata
and PRTG; and SIEMs (Security information and Event Management) systems such as Elasticsearch and Splunk; and other data sources

- Logging Dashboard with Graphana open source analytics and iteractive visualization web application.
- it provides charts, graphs, and alerts for the web when connected to supported data sources
- Grafana Eterprise version with additional capabilities is also available
- It is expandable through a plug-in system
- End users can create complex monitoring dashboards using interactive query builders.
- 
#### Downtime
- Downtime is the enemy
- Always try to minimize it
- It's the time when the system is down

#### Uptime
- The amount of time a system has been up per year, usually referred to as "five nines", "six nines", etc...
- 5x9 == 5min 15sec of annuall downtime
- 6x9 == 31 seconds of annual downtime
- 7x9 == 3seconds of annual downtime

how to calculate uptime/downtime?
```
365(days) * 24 (hrs) * 60 (min) = 525,600 per year
5x9 uptime = 0.99999 = ...
1 - 0.99999 = 0.00001 downtime
525.600 * 0.00001 = 5.256 minutes downtime per year
```
