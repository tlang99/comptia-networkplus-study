### Ethernet Fundamentals

[[#^411d16|Ethernet]] is the preferred Layer 2 protocol in modern networks.

Networks control access to the medium in one of two ways:
* [[#^88ddb0|Deterministic]]: orderly, devices take turns, no collisions
* [[#^8960ac|Contention-based]]: devices compete for access, so collisions can occur. Ethernet IS contention-based.

Ethernet manages contention with [[#^c0f41f|CSMA/CD]], which breaks down into three parts:
* CS, [[#^320a0c|Carrier]] Sense: a device listens to the medium to see if another node is transmitting, and waits if the line is busy
* MA, Multiple Access: any connected device can attempt to access and share the medium when it's free
* CD, Collision Detection: if two devices transmit at the same time, a collision happens. Both detect it, stop transmitting immediately, and each waits a random amount of time, the [[#^47b6ec|random backoff timer]], before retransmitting.

### Collision Domains

Devices that share a [[#^534793|collision domain]] operate in half-duplex mode, such as devices connected to a hub. Collision domains need to be kept small.

[[OBJ. 1.2#^d4e8b6|Switches]] increase scalability by creating multiple collision domains, one per port. Devices connected to a switch operate in full-duplex mode.

### Broadcast Domains

A [[#^6d50ca|broadcast domain]] is every device that receives a broadcast sent by any one of them. Switches forward broadcasts out every port, so they don't split broadcast domains. Routers don't forward broadcasts, so each router interface is its own broadcast domain. [[VLANs]] can also split broadcast domains on a switch.

### Speed and Duplex

[[#^4341a4|Speed and duplex configurations]] set how fast devices send data and how they communicate:
* [[#^8ea423|Half-duplex]]: send or receive, one at a time
* [[#^22e81e|Full-duplex]]: send and receive at the same time
* [[#^840be0|Auto-negotiation]]: devices pick the highest settings they have in common

In certain situations, such as with legacy equipment, you'll still want to configure speed and duplex manually.

### MTU and Jumbo Frames

The [[#^8a0209|Maximum Transmission Unit (MTU)]] is the largest packet or frame that can be sent over a network, measured in bytes. Getting it wrong either way causes problems:
* Too high: packets may be too large for the network to handle, which can lead to packet loss
* Too small: increased overhead

| Connection | MTU |
| --- | --- |
| Wired Ethernet | 1500 bytes, the standard and generally acceptable |
| Wireless, VPN, or PPPoE | Smaller, 1400–1420 bytes is a good size, since their encapsulation adds extra headers |
| [[#^00a0f3\|Jumbo frames]] | Usually 9000 bytes |

Jumbo frames help with storage area networks, large file transfers, video streaming, and server-to-server communication. Their downsides:
* Not all equipment supports them, so a bad configuration causes problems
* Fragmentation: a jumbo frame that hits a segment with a smaller MTU has to be split up
* Harder troubleshooting, since many tools don't support jumbo frames

### Glossary

Ethernet: The preferred Layer 2 protocol used in modern networks. A contention-based protocol. ^411d16

Deterministic: Network access that is very organized and orderly. A device that wants to transmit must wait its turn, so there are no collisions. This can limit data speed, since transmit time is split up, throttling devices. ^88ddb0

Contention-based: Network access where devices compete to communicate on the network at any given time. Collisions can occur if multiple devices transmit at once, which can be chaotic. ^8960ac


Carrier Sense Multiple Access with Collision Detection (CSMA/CD): The method Ethernet uses to share the medium. Devices listen before transmitting, any device can transmit when the medium is free, and devices that collide stop and retry after a random backoff timer. ^c0f41f

Random Backoff Timer: The random amount of time each device waits after a collision. When the timer hits 0, the device attempts to retransmit. ^47b6ec

Collision Domain: An area of the network that shares a single segment. ^534793

Carrier: A signal that carries information or data. ^320a0c

Broadcast Domain: A logical network segment where a broadcast message sent by any connected device reaches all other devices in that same segment. ^6d50ca

Speed and Duplex Configurations: Settings that determine the rate at which data is transmitted and the mode of communication between network devices. Duplex refers to how data is sent, either half-duplex or full-duplex. ^4341a4

Half-Duplex: Data transmission and reception can't happen at the same time. A device can only send or receive at once. ^8ea423

Full-Duplex: A device can send and receive simultaneously. ^22e81e

Auto-Negotiation: Allows devices to select the highest-performance settings they have in common. ^840be0

Maximum Transmission Unit (MTU): The largest size of a data packet or frame that can be sent over a network, measured in bytes. The standard on wired Ethernet is 1500 bytes. ^8a0209

Jumbo Frames: Any frame that exceeds the standard Ethernet MTU of 1500 bytes. Generally configured to a default size of 9000 bytes. ^00a0f3
