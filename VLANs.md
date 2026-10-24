### Virtual Local Area Networks

A [[#^0c4c32|VLAN]] logically splits a network into separate [[Ethernet Fundamentals#^6d50ca|broadcast domains]] through software configuration instead of physical cabling. VLANs are configured on a switch, so they operate at Layer 2. The switch tags each frame with a VLAN ID as it passes through, and as frames pass between switches, that ID determines which path they can take.

VLANs provide:
* Enhanced security: sensitive info can be isolated in its own VLAN, reducing the chance of a data breach
* Improved performance: smaller broadcast domains mean less traffic on each segment
* Increased management: separate controls can be applied to each VLAN
* Improved cost efficiency: fewer physical switches and less hardware are needed

Each switch keeps a [[#^74c72d|VLAN database]] with its VLAN configs:
* VLAN identifier
* VLAN name
* MTU size

Cisco switches store their database in the VLAN.DAT file.

A [[#^28c5ec|Switch Virtual Interface (SVI)]] lets the switch route traffic between VLANs without a separate router.

Summary: a VLAN segments Layer 2 traffic into separate broadcast domains, and it relies on the VLAN database and the SVI.

### VLAN Configurations

* [[#^2a3da4|802.1Q tagging]]: inserts a VLAN tag into each frame so switches forward it to the right VLAN
* [[#^a18a2d|Trunking]]: carries traffic from multiple VLANs over one link, kept separate by 802.1Q tags
* [[#^d1dd8b|Native VLAN]]: the one VLAN on a trunk that isn't tagged. VLAN 1 by default.
* [[#^8c5e53|Voice VLAN]]: a dedicated VLAN that separates VoIP traffic for better call quality
* [[#^12b1b9|Link aggregation]]: bundles multiple cables into one logical link, commonly used for trunk links between switches

802.1Q tagging is used to create logical separations between different departments.

### Glossary

Virtual Local Area Network (VLAN): A logical subdivision of a network that segments it into separate broadcast domains, using software configuration rather than physical cabling. Configured on a switch, so it operates at Layer 2. ^0c4c32

VLAN Database: Holds all of the VLAN configs for a switch: the VLAN identifier, VLAN name, and MTU size. Cisco switches store it in the VLAN.DAT file. ^74c72d

Switch Virtual Interface (SVI): Allows a switch to route traffic between different VLANs without requiring a separate router. Once an SVI is configured for a VLAN, the switch can handle routing decisions for that VLAN's traffic. ^28c5ec

802.1Q (VLAN) Tagging: An IEEE standard for managing multiple VLANs on a single network. Inserts a VLAN tag into each frame so switches can identify it and forward it to the proper VLAN. Each tag contains a VLAN ID (VID) that distinguishes one VLAN from another. Allows trunking to occur. ^2a3da4

Trunking: Transmitting traffic from different VLANs across the same physical link, while keeping each VLAN's traffic separate and secure. ^a18a2d

Native (Default) VLAN: The one VLAN on a trunk port whose frames are not tagged with a VLAN identifier when they cross a trunk link. Any untagged frame is placed in this VLAN, and legacy equipment that doesn't recognize VLAN tags can use it. Ex. if VLAN 10 is assigned as the native VLAN on a trunk port, untagged traffic is automatically assigned to VLAN 10. Must be configured consistently across all interconnected switches. VLAN 1 by default. ^d1dd8b

Voice VLAN: A specialized VLAN dedicated to voice traffic, particularly VoIP. Separates voice traffic from regular traffic to ensure the quality and reliability of calls, since voice is especially sensitive to delays. Improves call quality, latency, jitter, and packet loss. ^8c5e53

Link Aggregation: Also known as port channeling or bonding. Combines multiple network connections into a single logical link that shares their bandwidth. Ex. with one 1 Gbps cable between two switches, if it fails the devices on each side can't communicate. With four 1 Gbps cables and link aggregation, they're treated as essentially one cable and share their bandwidth. Commonly used for trunk links between switches. ^12b1b9
