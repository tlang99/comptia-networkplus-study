The Network Layer handles forwarding traffic (routing) using logical addresses ([[#^a2c5e8|IPv4]] or [[#^b4d7f9|IPv6]] addresses). IP is considered a Layer 3 protocol, and data at this layer is known as a Packet.

Other logical addressing protocols exist, but IP is by far the most popular. AppleTalk and IPX were also used, but neither is important for the exam, since IP killed them off.

"Switching" at Layer 3 refers to routing, not to be confused with the term switching used at Layer 2. The switching methods at this layer are:
* [[#^0c3e61|Packet Switching]]
* [[#^1d4f72|Circuit Switching]]
* [[#^2e5a83|Message Switching]]

Routes are handled through [[#^3f6b94|Route Discovery and Selection]]. Layer 3 also provides [[#^4a7ca5|Connection Services]], including [[#^5b8db6|Packet Reordering]], and uses [[#^6c9ec7|ICMP]] to send error messages and operational information.

Layer 3 devices include routers and [[#^7dafd8|multi-layer switches]].

### Glossary

IPv4: A binary, logical addressing protocol split into 4 octets. ^a2c5e8

IPv6:  ^b4d7f9

Packet Switching: The most common method, used in most scenarios. Data is divided into packets and then forwarded based on its IP address. Packets can take any path as long as they reach the recipient. ^0c3e61

Circuit Switching: A dedicated communication link is established between two devices. It uses the same path every single time. ^1d4f72

Message Switching: Data is divided into messages, which may be stored and then forwarded. ^2e5a83

Route Discovery and Selection: Routes are either manually configured as a static route, or learned dynamically through a routing protocol, like RIP, OSPF, or EIGRP. ^3f6b94

Connection Services: Augment Layer 2 connection services to improve reliability by utilizing flow control and [[#^5b8db6|packet reordering]]. ^4a7ca5

Packet Reordering: Ensures that all data reaches the receiver correctly at the end destination. ^5b8db6

Internet Control Message Protocol (ICMP): Sends error messages and operational information to an IP destination. The most commonly used ICMP tools are `ping` and `tracert`. ^6c9ec7

Multi-layer Switch: Has the features of both a Layer 2 switch and a router. A switch is ALWAYS a Layer 2 device unless it is a multi-layer switch, in which case it is a Layer 3 device. ^7dafd8
