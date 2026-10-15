### Network Geography

Network geography is about the distance involved. From smallest to largest, networks are classified as:
* [[#^3d9f12|Personal Area Network (PAN)]]
* [[#^7a4c55|Local Area Network (LAN)]]
* [[#^b81e07|Campus Area Network (CAN)]]
* [[#^2f6d94|Metropolitan Area Network (MAN)]]
* [[#^e5c3a8|Wide Area Network (WAN)]]

A PAN usually covers a distance of about 10 feet or less. Ex. Bluetooth and USB. Bluetooth transmitting music to your car sound system is an example of a PAN. Another is connecting a USB drive to a computer.

A LAN covers up to about 300 feet or 100 meters. Ex. Home, floor of an office building, classroom.

A CAN can cover several miles and many buildings. Ex. College campuses may utilize a CAN to link multiple LANs across multiple buildings. CANs are also used by military bases or business parks.

A MAN is larger than a CAN, but smaller than a WAN. Ex. Separate campuses of one college may connect their CANs/LANs via a MAN.

A WAN covers a very large geographic area. Ex. Country, or even the world. Ex. Leased lines, virtual private networks. The Internet is a WAN, and the largest WAN at that, but a WAN does not always need to be public like the Internet.

Networks consist of either Wi-Fi or Ethernet. Wi-Fi utilizes the IEEE 802.11 Standard, and Ethernet utilizes the IEEE 802.3 Standard.

### Wired Network Topology

[[#^91b7f0|Network Topology]] is documented in diagrams using either a [[#^4c2e6a|Physical Topology]] or a [[#^d07a39|Logical Topology]]. A logical diagram doesn't show the actual physical location of the devices or use a floor plan.

The main topologies are:
* [[#^68f1c4|Point-to-point]]
* [[#^a3e95d|Ring]]
* [[#^c64d0e|Bus]]
* [[#^5b9a73|Star]]
* [[#^f2d618|Hub-and-spoke]]
* [[#^0e7c4b|Mesh]]

Point-to-point is often used for connecting computers to a peripheral like a scanner or printer.

In a Ring Topology, data travels in one direction around the circle until it reaches its destination, which prevents data collisions. However, if one node fails, it can disrupt the whole network. Ring is not very common, unless used in [[#^1f8b26|Fiber Distributed Data Interface (FDDI)]], which operates on a dual ring structure to provide redundancy.

In a Bus Topology, data can be sent by any device and is available to every other device on the bus, but only the intended recipient can receive data. It is easy to install and uses less cable, but the entire network can be disabled if the bus fails, and more traffic can cause data collisions. Bus is not common, and is older tech.

Star is one of the most common topologies, used often in homes. It is very robust, since failure of one link does not disrupt others, but if the central connection point fails, the whole network can be disrupted.

In Hub-and-spoke, spokes are not directly connected, and must transmit data to a hub which then relays it. It is commonly used in airlines. For example, multiple offices in a city may transmit data to a nearby hub. Said hub will then transmit to another distant hub, where it's then distributed to all of the linked devices on that one.

Mesh comes in two forms:
* [[#^8a35d1|Full-mesh]]
* [[#^47bf92|Partial-mesh]]

Full-mesh can be expensive and difficult to install in larger environments. The number of connections in a full mesh is:
x = n(n-1)/2 where *n= number of nodes*

In a partial mesh, more important nodes may be connected to all nodes, while less critical nodes may only be connected to crucial ones.

Summary:
* Point-to-point: Simple, reliable for small scale connections
* Ring and Bus: Simple, vulnerable to single points of failure
* Star and Hub-and-spoke: Centralized, however rely heavily on the hub/central point
* Mesh: Robustness, redundancy, but complex and costly for full mesh. Partial mesh gives up some redundancy

### Data Center Topology

A [[#^b3a06e|Data Center]] can vary widely in size, from 150 square feet to 1.5 million square feet like the Utah Data Center. Data centers utilize the following topologies:
* [[#^9c1f5a|Three-Tiered Hierarchy]]
* [[#^a8f263|Collapsed Core]]
* [[#^0b5e9d|Spine and Leaf Architecture]]

The Three-Tiered Hierarchy consists of three layers:
* [[#^26e8b4|Core]]
* [[#^e94a17|Distribution/Aggregation]]
* [[#^53d7c0|Access/Edge]]

It provides redundancy and reliability, since one device can be down while the rest of the network functions as normal.

In a Collapsed Core, the functions of the distribution and core layers are combined, simplifying architecture. It is found in small or medium sized data centers where three tiered is not needed, and is not suitable for larger and more complex networks.

Spine and Leaf Architecture is made up of two layers:
* [[#^7d2a41|Spine]]
* [[#^c3f87b|Leaf]]

It offers faster speeds and lower latency than three-tiered, and works well with Software Defined Networking. It can also be used in combination with three-tiered: all the servers connect to leaf layers, which connect to the spine, which connects to the core layer of the three-tiered model.

Traffic Flows describe how data moves in and around a data center:
* [[#^15a6e9|North-South]], which is either [[#^6f0d3c|Northbound]] or [[#^92c8a5|Southbound]]
* [[#^d5b14f|East-West]]

### Glossary

Personal Area Network (PAN): Smallest type of wired or wireless network which usually covers a distance of about 10 feet or less. ^3d9f12

Local Area Network (LAN): Connects components in a limited distance, up to about 300 feet or 100 meters. ^7a4c55

Campus Area Network (CAN): Connects multiple LANs that are spread across numerous buildings in a certain area. ^b81e07

Metropolitan Area Network (MAN): Connects locations that are scattered across the entire city. ^2f6d94

Wide Area Network (WAN): Connects geographically disparate internal networks. ^e5c3a8

Network Topology: Refers to the arrangements of different elements like links, nodes, clients, and servers that make up a computer network. ^91b7f0

Physical Topology: Used to show how the network devices and components are physically cabled and connected together and where they're located in the real world environment. ^4c2e6a

Logical Topology: Talks about how the traffic is actually going to flow in the network. Demonstrates the way the data flows between the devices. ^d07a39

Point-to-point: Simplest form of topology that involves a direct connection between two devices. ^68f1c4

Ring Topology: A network configuration where each device is connected to two other devices, forming a circular data path. ^a3e95d

Fiber Distributed Data Interface (FDDI): Used to conduct data transmissions on fiber optic lines in a local area network. Operates on a dual ring structure to provide redundancy. ^1f8b26

Bus Topology: All of the network devices are connected to a single, central cable, called the bus or backbone. ^c64d0e

Star Topology: Each node connects back to a central connection point, like a switch. ^5b9a73

Hub-and-spoke Topology: Variation of the Star Topology where the central node (hub) is connected to multiple nodes (spokes). ^f2d618

Mesh Topology: Features a point-to-point connection between every single device on the network to create a robust and redundant network. ^0e7c4b

Full-mesh: Every node is connected to every other node in the network. ^8a35d1

Partial-mesh: Some nodes are organized in a full mesh scheme, while others are only connected to one or two devices in the network. ^47bf92

Data Center: Any facility used by businesses to organize, process, store, and disseminate large amounts of data. ^b3a06e

Three-Tiered Hierarchy: Data center topology that consists of three layers: Core, Distribution/Aggregation, and Access/Edge. ^9c1f5a

Core: Backbone of network, merges geographically separated networks back into one cohesive unit. Have at least two routers that operate in a redundant configuration. ^26e8b4

Distribution/Aggregation: Under the core layer, implements access lists and filters. Defines the policies for the network. Switches will be found here routing to different subnets and VLANs. ^e94a17

Access/Edge: Beneath the distribution layer, connects all endpoint devices. Switches found here, converts packets to frames and ensures they're delivered to correct endpoints. ^53d7c0

Collapsed Core: Network architecture where the core and distribution layers are merged into a single layer, giving a two-tiered system. ^a8f263

Spine and Leaf Architecture: Alternative type of network architecture that focuses on the communication within the data center itself. ^0b5e9d

Spine: Connects switches, creating a full mesh topology. ^7d2a41

Leaf: Consists of all access switches, aggregates traffic from different servers and connects into the spine. ^c3f87b

North-South: Traffic enters or leaves the data center from a system residing outside of the data center. ^15a6e9

Northbound Traffic: Leaving data center. ^6f0d3c

Southbound Traffic: Entering data center. ^92c8a5

East-West: Refers to data flow within a data center. ^d5b14f
