### Routers

A [[#^5bca66|router]] forwards traffic between subnets, between internal and external networks, or between two external networks. Each subnet or external network connected to it is its own broadcast domain.

NOTE: A multilayer (Layer 3) switch can also route, so on the exam, treat it like a router when a question is about routing.

### How Traffic Moves Between Networks

Ex. PC1 on one network sends data to PC2 on another network:
1. PC1 compares PC2's IP address to its own subnet. PC2 is on a different network, so PC1 sends the traffic to its [[#^12052e|default gateway]] (the router).
2. PC1 uses [[#^140e3f|ARP]] to find the router's MAC address (not PC2's), then sends a frame addressed to the router's MAC.
3. The switch forwards the frame to the router using its MAC address table.
4. The router strips off the frame (decapsulation), reads the destination IP address in the packet, and looks it up in its [[#^96758f|routing table]].
5. The router puts the packet in a new frame and forwards it to the next hop, another router.
6. On PC2's network, the last router uses ARP to find PC2's MAC address, then sends the frame to PC2.

The key point: the source and destination IP addresses stay the same the whole way. The MAC addresses change at every hop.

### Routing Tables

A [[#^96758f|routing table]] tells a router where to send traffic for each destination network. Each route entry contains:
* Destination network
* Next hop (the next router)
* Interface (port)
* Route cost ([[#^bf040e|metric]])

When more than one route matches, the router picks one in this order:
1. [[#^d1d72c|Longest prefix match]]: the most specific route wins. Ex. 10.1.1.0/24 is more specific than 10.0.0.0/8.
2. [[#^0ce622|Administrative distance]]: if the same network is learned from different sources, the most trusted source wins.
3. [[#^bf040e|Metric]]: if the same source offers more than one route, the lowest cost wins.

Administrative distance (AD) rates how believable a route's source is. Lower AD is more believable. From most to least believable:
1. Directly connected
2. Static
3. EIGRP
4. OSPF
5. RIP
6. External EIGRP
7. Unknown (unbelievable)

NOTE: Dion says you don't need to memorize this order for the exam, but have a general idea of what's more believable. Generally, the newer the protocol, the more believable. Ex. RIP is older, so it's less believable than OSPF.

AD is separate from the metric. Within one routing protocol, lower metrics are preferred over higher ones. Ex. the fewest hops is best.

### Route Types

Routes get into the routing table four ways:
* [[#^7c702e|Directly connected route]]: a network attached to one of the router's own interfaces
* [[#^e5ae19|Static route]]: manually configured by an administrator
* [[#^3d8162|Default static route]]: 0.0.0.0/0, "if you don't know where to go, go here"
* [[#^0bdeee|Dynamic route]]: learned from other routers through a [[Routing Protocols|routing protocol]]

### Preventing Routing Loops

Two methods prevent [[#^6aec7b|routing loops]]:
* [[#^0e444c|Split horizon]]: a route learned on an interface is never advertised back out that interface
* [[#^869f92|Poison reverse]]: a route learned on an interface is advertised back out that interface with an infinite metric

### Glossary

Router: A Layer 3 device that forwards traffic between subnets, between internal and external networks, or between two external networks. Each network it connects is its own broadcast domain. ^5bca66

Default Gateway: The router a device sends traffic to when the destination is on a different network. ^12052e

Address Resolution Protocol (ARP): Finds the MAC address that belongs to an IP address on the local network. ^140e3f

Routing Table: A list of routes a router uses to decide where to send traffic. Each entry lists the destination network, next hop, interface, and metric. It maps destination networks to where traffic should go next, not IP addresses to MAC addresses (that's ARP). ^96758f

Longest Prefix Match: When several routes match a destination, the one with the longest prefix (most specific network) is used. Ex. a /24 route beats a /8 route. ^d1d72c

Administrative Distance (AD): A rating of how believable, or trustworthy, a route's source is. When the same network is learned from different sources, the lowest AD wins. Directly connected routes are the most believable, then static routes, then dynamic routing protocols. ^0ce622

Metric (Route Cost): The value a routing protocol uses to compare routes to the same destination, like hop count or bandwidth. Lower is better. ^bf040e

Directly Connected Route: A route to a network attached directly to one of the router's interfaces. The router learns it automatically. ^7c702e

Static Route: A route manually configured by an administrator. ^e5ae19

Default Static Route: 0.0.0.0/0. Used when no other route matches: "if you don't know where to go, go here." ^3d8162

Dynamic Route: A route learned by exchanging information with other routers, using a routing protocol. ^0bdeee

Routing Loop: When packets bounce between routers endlessly because their routing tables point at each other. ^6aec7b

Split Horizon: Prevents a route learned on one interface from being advertised back out that same interface. If a route came in on an interface, it can't go back out that interface. ^0e444c

Poison Reverse: A route learned on one interface is advertised back out that same interface with a metric considered infinite. This tells the neighbor never to send traffic for that network back through this router, since the route is too expensive. ^869f92
