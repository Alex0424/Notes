# General Ops

## On-Prem Hosting

The easiest explanation: put a server up in a room and run it.

Own your hardware (or potentially lease it).

Be responsible for all the applications and systems uptime.

Have control over the whole process.

You own your data.


### Ops - Hardware

Relevant when hosting on-prem OR when renting datacenter space(co-location) where to put your hardware.

Things break, what to do then?: be ready and have a plan before this happends.

handle warranties, reliability, maintainability, and availability without leaking data.

Order new hardware
- make sure to order the right thing!
- delivery time
- somone needs to drive to the datacenter and mount the hardware
- - inventory
  - archive invoices/warranties/etc

Hardware upgrades
- monitor server health
- be proactive

Upgrades and new hardware
- expensive
- which service contract? (terms, ...)
- how long should the newly bought hardware "live"?
- when to upgrade? EOL (end of life) (plan when to upgrade)

inventory(whichever system you use [document all systems])
- keep an inventory of all your hardware (address, place, name, pwd, ...)

### Ops - Choosing the right place

Self-hosting, where to put the servers?

own datacenter (are we operating at the right scale)

co-location in somone else's datacenter(how about security?)

#### Security
- natural catastrophes
- security from theft(both physical and data)
- your servers are loud

#### Electricity
- do we have enough to power everything in the datacenter?
- how do we deal with breakouts?

#### Temperature
- how do you plan on controlling the temp in the datacenter?
- rising temperatures becomes a problem quickly
- - reduced performance (throtting)
  - instability and crashes
  - shortens the lifespan of your hardware

#### Network
- stable connection with enough bandwidth/throughput outwards
- cable handling


# Ops - Uptime

How important is it for your applications?

Keep in check:
- fault tolerance
- redundancy

How much load does your system handle before impacting on uptime?

On prem == 100% your responsibility.

On the cloud == at least can take hardware out the equation.

# Ops - Security

LEAST. PRIVILEGE. PRINCCIPLE. ALWAYS!

Deploy & Upgrade routines:
- test enviroment first! (sometimes newer version can have bugs)

CVEs, keep up with those
- do they affect you / your products?
- do they affect your providers/their products?
- do they affect their providers/their products?

Security patches, keep up with those
- sometimes they compromise on performance (specter, meltdown)
- security upgrades are important (look at change log)

# Ops - Network

