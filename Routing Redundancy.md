### Routing Redundancy Protocols

A [[#^b84d62|routing redundancy protocol]] prevents disruptions in communication by automatically rerouting traffic when a path or device fails.

A [[#^612e4f|First Hop Redundancy Protocol (FHRP)]] provides three main benefits:
* Reliability: communication stays up even if a single router fails
* Load balancing: distributes network traffic across multiple routers so no single device is overwhelmed
* Seamless transitions: traffic from a failed router is redirected to a standby router seamlessly

FHRPs rely on two things:
* [[#^c71e9c|Virtual IP]]
* [[#^4de880|Subinterface]]

### FHRP Protocols

The three main FHRPs:

| Protocol | Standard | Key feature |
| --- | --- | --- |
| [[#^ced815\|HSRP]] | Cisco | One active router and one standby, with [[#^670eb5\|preempting]] |
| [[#^ba9d92\|VRRP]] | Open standard | Works like HSRP, with multiple routers and a simple, automatic election |
| [[#^e17c80\|GLBP]] | Cisco | Adds load balancing |

Summary: routing redundancy protocols provide reliability and efficiency. HSRP, VRRP, and GLBP all keep data flowing within the network even if a router goes down.

### Glossary

Routing Redundancy Protocol: A network protocol that prevents disruptions in communication by automatically rerouting traffic when a path or device fails. ^b84d62

First Hop Redundancy Protocol (FHRP): A set of protocols that keeps a network reliable by providing automatic failover to a backup router. It detects when the primary router fails and automatically routes to a standby router instead. ^612e4f

Virtual IP: An IP address that isn't bound to a specific device, but represents one or multiple devices. ^c71e9c

Subinterface: Divides a single interface on a switch or router into multiple logical interfaces. Cost-efficient, and helps with traffic management. ^4de880

Hot Standby Router Protocol (HSRP): A Cisco redundancy protocol that establishes a fault-tolerant default gateway for devices on a local network segment. One router is elected the active router and one the standby router. ^ced815

Preempting: In HSRP, a higher-priority router takes over as the active router if it comes online after the initial election. ^670eb5

Virtual Router Redundancy Protocol (VRRP): An open standard redundancy protocol that functions similarly to HSRP, with a few differences: it supports multiple routers and has a simple, automatic election scheme. ^ba9d92

Gateway Load Balancing Protocol (GLBP): A Cisco protocol that adds load balancing. Allows multiple routers to provide redundancy for the virtual IP address assigned to a group of routers. ^e17c80
