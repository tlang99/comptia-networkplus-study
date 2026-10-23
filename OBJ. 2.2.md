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

### Glossary

Ethernet: The preferred Layer 2 protocol used in modern networks. A contention-based protocol. ^411d16

Deterministic: Network access that is very organized and orderly. A device that wants to transmit must wait its turn, so there are no collisions. This can limit data speed, since transmit time is split up, throttling devices. ^88ddb0

Contention-based: Network access where devices compete to communicate on the network at any given time. Collisions can occur if multiple devices transmit at once, which can be chaotic. ^8960ac

Carrier Sense Multiple Access with Collision Detection (CSMA/CD): The method Ethernet uses to share the medium. Devices listen before transmitting, any device can transmit when the medium is free, and devices that collide stop and retry after a random backoff timer. ^c0f41f

Random Backoff Timer: The random amount of time each device waits after a collision. When the timer hits 0, the device attempts to retransmit. ^47b6ec

Collision Domain: An area of the network that shares a single segment. ^534793

Carrier: A signal that carries information or data. ^320a0c
