### Network Components

A network is made up of components that work together to move data between users and the resources they need. These include:
* Clients
* Servers
* Hubs
* Switches
* Wireless Access Points (WAPs/APs)
* Routers
* Firewalls
* Load Balancers
* Proxies
* Intrusion Detection Systems (IDS) & Intrusion Prevention Systems (IPS)
* Controllers
* Network-attached Storage (NAS) devices
* Storage Area Networks (SANs)
* Media
* Wide Area Network (WAN) links

Users access the network through [[#^a1c3e9|Clients]], which use the resources provided by [[#^b27d40|Servers]].

Devices on a local area network were originally connected with [[#^c9f1a2|Hubs]]. Hubs are not commonly used in modern networks, but they are still relevant for the exam. Because they broadcast everything they receive, they are prone to network errors. Hubs evolved into bridges, and then into [[#^d4e8b6|Switches]], which forward traffic only to the destination port, making them more efficient and secure. [[#^e06f3c|Wireless Access Points]] do a similar job for wireless devices, connecting them to the wired network. Like hubs, they broadcast data, but over radio signals instead of copper or fiber cable.

To connect separate networks together, a [[#^f5a291|Router]] is used. Routers rely on the Internet Protocol and make forwarding decisions based on the IP addresses of the devices communicating.

Several components protect the network. A [[#^1b7c4d|Firewall]] controls traffic between the internal network and external networks, usually the internet. An [[#^2e9a03|IDS]] watches for unauthorized access or anomalies and alerts administrators, while an [[#^3f60b8|IPS]] does everything an IDS does and also takes action to stop the intrusion. A [[#^4a2d71|Proxy]] sits between users and the internet and provides:
* Web filtering
* Shared network connections
* Data caching
* Enhanced security and privacy

To keep the network performing well, a [[#^5c8e19|Load Balancer]] spreads traffic across multiple servers to prevent bottlenecks, and [[#^6d0f42|Controllers]] centrally manage flow control to networking devices.

Data can be stored centrally in two ways: a [[#^7e31a5|NAS]] device provides file-level access to clients, while a [[#^8f4b9c|SAN]] is a dedicated high-speed network that provides block-level storage.

All of this data travels over [[#^90c6d2|Media]], and networks spread across large geographic areas are joined using [[#^a7e215|WAN Links]].

### Network Resources

Resources are shared on a network using one of two main models:
* [[#^b8f530|Client/Server Model]]
* [[#^c19d64|Peer-to-Peer Model]]

The Client/Server Model is the leading model in business networks. Its pros:
* Centralized administration
* Easier management
* Better scalability

Its cons:
* Costs more
* Requires dedicated OSes
* Requires a specialized skillset

The Peer-to-Peer Model is cheaper and simpler. Its pros:
* Lower cost
* No specialized OS
* No dedicated resources

Its cons:
* Administration is difficult, since files are spread across different machines in different places
* Scalability is difficult for the same reason
* If a machine is off, its files may be inaccessible
* Inefficient for large networks

### Glossary

Clients: Devices that users access the network with. Ex. Laptops, workstations, smartphones, and tablets. ^a1c3e9

Servers: Provide resources to other clients on the network. Ex. Email servers, file servers, and media servers. ^b27d40

Hubs: Older devices that connect clients and servers over a local area network by broadcasting all traffic out every port. ^c9f1a2

Switches: "Smarter hubs" that connect network devices and forward traffic from one port to the destination port. ^d4e8b6

Wireless Access Points (WAPs/APs): Allow wireless devices to connect to a wired network using radio signals. ^e06f3c

Routers: Connect different networks together and make forwarding decisions based on IP addresses. ^f5a291

Firewalls: Security barriers between internal and external networks that monitor and control incoming and outgoing traffic. Can be hardware-based, software-based, or both. ^1b7c4d

Intrusion Detection System (IDS): Detects unauthorized access or anomalies and alerts administrators. ^2e9a03

Intrusion Prevention System (IPS): Does everything an IDS does, and also takes action to prevent the intrusion. ^3f60b8

Proxy: An intermediary between a user's device and the internet. ^4a2d71

Load Balancers: Devices or software that distribute traffic across multiple servers so no single server bears too much demand. ^5c8e19

Controllers: Central units used to manage flow control to networking devices. ^6d0f42

Network-attached Storage (NAS): Dedicated file storage system that provides file-level data access to a wide variety of clients. ^7e31a5

Storage Area Network (SAN): High-speed network that provides access to consolidated block-level data storage. ^8f4b9c

Media: Physical materials used to transmit data. ^90c6d2

Wide Area Network (WAN) Links: Used to connect networks over large geographical areas. ^a7e215

Client/Server Model: Uses a dedicated server to provide access to network resources, such as files, scanners, and printers. ^b8f530

Peer-to-Peer Model: Peers (Ex. laptops, desktops) share resources directly with each other, without a dedicated server. ^c19d64
