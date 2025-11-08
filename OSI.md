# OSI Model

## OSI Layers

```mermaid
graph TD
1["1. Physical"]
2["2. Data Link"]
3["3. Network"]
4["4. Transport"]
5["5. Session"]
6["6. Presentation"]
7["7. Application"]

7 <--> 6 <--> 5 <--> 4 <--> 3 <--> 2 <--> 1
```

### 4. Transport

Transmits data using transmission protocols including TCP & UDP

### 3. Network

Decides which physical path the data will take.

Routing data and logical addressing (e.g. IP), determining the best path from source to destination across networks.

### 2. Data Link

Defines the format of data on the network

1. Receives data from physical layer
2. Checks for transmission errors
3. Packages bits to data frames (e.g.: `| MAC1 | MAC2 | IP1 IP2 Segment | FCS`)
4. Manages the physical addressing layer:
  - Media Access Control (MAC)
  - Logical Link Control (LLC)

### 1. Physical

Transmission and reception of raw bitstreams over a physical medium.

Examples: network cable, power plug, cable pinouts, wireless radio frequencies, Transceivers, repeaters, pulses of light etc.



## Links

https://youtu.be/Ilk7UXzV_Qc

https://youtu.be/oVVlMqsLdro

https://www.cloudflare.com/en-gb/learning/ddos/glossary/open-systems-interconnection-model-osi/

