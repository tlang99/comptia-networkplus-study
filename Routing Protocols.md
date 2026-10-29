### Interior vs. Exterior

Dynamic routing protocols are one of two types:
* [[#^2ebc1e|Interior Gateway Protocol (IGP)]]: operates within an [[#^63673c|autonomous system (AS)]]
* [[#^e35178|Exterior Gateway Protocol (EGP)]]: operates between autonomous systems

### Advertisement Methods

Routing protocols share routes in one of these ways:
* [[#^8349fe|Distance vector]]: sends its full routing table to its neighbors at regular intervals. Only counts [[#^8aa794|hops]], not link speed. Slow [[#^18932e|convergence]].
* [[#^a8c02d|Link state]]: every router knows the paths every other router can reach. Faster convergence than distance vector.
* [[#^752b27|Hybrid]]: combines distance vector and link state features
* [[#^109a78|Path vector]]: counts autonomous system hops instead of router hops

Once every router knows every other router's networks, you have a [[#^b38dcf|converged network]]. [[#^2135ef|Hold-down timers]] help keep the network stable while it converges.

### Routing Protocols

| Protocol | Method | Metric | Type | Notes |
| --- | --- | --- | --- | --- |
| [[#^d33f33\|RIP]] | Distance vector | Hop count, max 15 (16 = unreachable) | IGP | |
| [[#^5420b1\|OSPF]] | Link state | Cost, based on bandwidth | IGP | Open standard, very common |
| [[#^342cd0\|IS-IS]] | Link state | Cost | IGP | Works like OSPF, less popular |
| [[#^8fbd4f\|EIGRP]] | Hybrid | Bandwidth and delay | IGP | Cisco proprietary |
| [[#^78b423\|BGP]] | Path vector | Number of autonomous system hops | EGP | The backbone of the internet |

### Multicast Routing

[[#^649521|Multicast routing]] sends traffic to a Class D IP address, known as a multicast group. It uses two protocols:
* [[#^5f3485|IGMP]]: lets clients join a multicast group and tells routers which interfaces have receivers
* [[#^72d453|PIM]]: routes multicast traffic between routers and forms a distribution tree, in one of two modes:
	* [[#^8d7e63|Dense mode (PIM-DM)]]
	* [[#^27d41c|Sparse mode (PIM-SM)]]

### Generic Routing Encapsulation

[[#^f1317d|GRE]] creates a virtual point-to-point tunnel between two locations over an IP network:
* Operates at Layer 3 and is configured on the network's router
* Encapsulates many types of network protocols
* Simple, efficient, and more lightweight than a full site-to-site VPN
* Not encrypted on its own, so it's often combined with a VPN for security

### Glossary

Autonomous System (AS): A network or group of networks under a single organization's control, Ex. an ISP or a large company. ^63673c

Interior Gateway Protocol (IGP): A routing protocol that operates within an autonomous system. Ex. RIP, OSPF, IS-IS, EIGRP. ^2ebc1e

Exterior Gateway Protocol (EGP): A routing protocol that operates between autonomous systems. Ex. BGP. ^e35178

Distance Vector: Sends a full copy of its routing table to its directly connected neighbors at regular intervals. Has a slow convergence time. Doesn't consider link speeds, only the number of hops between it and the destination. ^8349fe

Link State: Requires all routers to know about the paths all other routers can reach in the network. Faster convergence time than distance vector. ^a8c02d

Hybrid: Combines features of distance vector and link state protocols. Ex. EIGRP. ^752b27

Path Vector: Chooses routes based on the number of autonomous system hops instead of router hops. Ex. BGP. ^109a78

Convergence: The time it takes for routers to update their routing tables after the topology changes. ^18932e

Converged Network: A network where all connected routers know all the information about each other's networks. ^b38dcf

Hold-down Timer: After a route goes down, the router ignores updates about that route for a set period of time. This keeps bad information from spreading and prevents routing loops, though it can slow convergence a little. ^2135ef

Hop Count: The number of routers data must pass through from the source router to get to its destination. ^8aa794

Routing Information Protocol (RIP): A distance vector, interior gateway protocol that uses hop count as its metric. Maximum of 15 hops; 16 is considered infinite (unreachable). ^d33f33

Open Shortest Path First (OSPF): A link state, interior gateway protocol that uses cost, based on link bandwidth, as its metric. An open standard and one of the most widely used IGPs. ^5420b1

Intermediate System to Intermediate System (IS-IS): A link state, interior gateway protocol that uses cost and functions like OSPF, but isn't as widely used. ^342cd0

Enhanced Interior Gateway Routing Protocol (EIGRP): A hybrid of distance vector and link state. An interior gateway protocol that uses bandwidth and delay as its metric. Proprietary to Cisco. ^8fbd4f

Border Gateway Protocol (BGP): A path vector, exterior gateway protocol that uses the number of autonomous system hops instead of router hops. The backbone of the internet. ^78b423

Multicast Routing: Sending traffic to a Class D IP address, known as a multicast group. ^649521

Internet Group Management Protocol (IGMP): Used by clients and routers to let routers know which interfaces have multicast receivers, and to let clients join a multicast group. ^5f3485

Protocol Independent Multicast (PIM): Routes multicast traffic between routers and forms a distribution tree. Runs in dense mode or sparse mode. ^72d453

PIM Dense Mode (PIM-DM): Uses periodic flood and prune behavior to form an optimal distribution tree. ^8d7e63

PIM Sparse Mode (PIM-SM): Uses a shared distribution tree, then creates an optimal distribution tree through the shortest path tree. ^27d41c

Generic Routing Encapsulation (GRE): A tunneling protocol that encapsulates a wide variety of network layer protocols inside virtual point-to-point links over an IP network. Operates at Layer 3 and is configured on the network's router. Useful for connecting similar topologies over a different intermediate network, creating a direct link between two locations. Not encrypted on its own, but can be combined with a VPN. ^f1317d
