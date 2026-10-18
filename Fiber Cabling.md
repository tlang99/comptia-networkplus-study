### Fiber Media

[[#^3d518a|Fiber media]] transmits data using light instead of the electrical impulses used by copper media.

Compared to copper, fiber:
* Is fully immune to EMI
* Has a much longer max range, spanning hundreds of miles with a single fiber optic cable
* Has much higher speeds, with most fiber optic cables operating between 10 and 1000 Gbps
* Is much more expensive and more complex, and more challenging to work with than twisted pair or coax

There are two main types of fiber-optic media:
* [[#^28186d|Single-Mode Fiber (SMF)]]
* [[#^ff5aab|Multi-Mode Fiber (MMF)]]

| | SMF | MMF |
| --- | --- | --- |
| Core size | 8.3 to 10 microns | 50 to 100 microns |
| Light paths | Single path | Multiple paths |
| Distance | Tens to hundreds of miles | Shorter distances |
| Sheath color | Yellow | Aqua blue or orange |
| Cost | More expensive | Cheaper |
| Used for | Backbone installations, large networks, connections between vast segments of land | Buildings, campuses, business parks |

### Fiber Connectors

Fiber connections have two different sets of connectors, one for the transmit side and one for the receive side. Some manufacturers make cables with paired fiber optic cores in a single jacket, connecting the transmit and receive ports.

The common fiber connectors are:
* [[#^15a73a|Subscriber Connector (SC)]]
* [[#^b98b62|Lucent Connector (LC)]]
* [[#^4d8066|Straight Tip Connector (ST)]]
* [[#^aea722|Mechanical Transfer-Registered Jack (MTRJ)]]
* [[#^c338d2|Multi-Fiber Push On (MPO)]]

| Connector | Shape | Mechanism | Remember it by |
| --- | --- | --- | --- |
| SC | Square | Push-pull | "Stick and click." Commonly used and durable |
| LC | Compact | Push-pull | Small size for high-density environments like data centers. Often shipped as a joined pair |
| ST | Round | Twist-lock | "Stick and twist." Handles movement, vibration, and outdoor weather. Common with MMF |
| MTRJ | Small, rectangular | Latch, like other RJ connectors | Transmit and receive fibers in one connector |
| MPO | | Push on | Usually 12 or more fibers in one connector. High-density data centers |

### Polishing and Back Reflection

[[#^4446d7|Back reflection]] happens when light reflects back into the transmitter, which degrades the signal. The type of polish used on the fiber end face affects back reflection as well as cost:
* [[#^06fde8|Physical Contact (PC)]]
* [[#^5a7d62|Ultra Physical Contact (UPC)]]
* [[#^cc33bb|Angled Physical Contact (APC)]]

| Polish | End face | Back reflection | Used for | Cost |
| --- | --- | --- | --- | --- |
| PC | Slight curvature | Most of the three (but lower than a straight cut) | Telephone services, lower speeds or short distances | |
| UPC | Dome shaped | Lower than PC | Broadband, data, and video | Good balance between performance and cost |
| APC | 8 degree angle | Least | Long-haul applications like undersea connections | Expensive |

### Glossary

Fiber Media: Media that transmits data using light instead of electrical impulses. Fully immune to EMI, with a much longer max range and much higher speeds than copper, but much more expensive and complex. ^3d518a

Single-Mode Fiber (SMF): Designed for long-distance communications. Features a small glass core, typically around 8.3 to 10 microns in diameter, smaller even than a human hair. Light can only travel down a single path. Spans tens to hundreds of miles. Used for backbone installations, large networks, and connections between vast segments of land. Wrapped in a yellow sheath. ^28186d

Multi-Mode Fiber (MMF): Tailored for shorter distances, with a larger fiber core that ranges from 50 to 100 microns. Light can travel down multiple paths. Cheaper than SMF. Used in buildings, campuses, and business parks. Wrapped in an aqua blue or orange sheath. ^ff5aab

Subscriber Connector (SC): Known for its square shape and push-pull design, which offers a secure and simple connection. Known as "stick and click," since you insert it until you hear the click. Commonly used and durable. ^15a73a

Lucent Connector (LC): Distinguished by its compact size. Uses a push-pull mechanism like the SC connector. Favored in high-density environments like data centers due to its small size. Often shipped as a two-cable pair with the connectors joined together. ^b98b62

Straight Tip Connector (ST): Recognized by its round shape and twist-lock mechanism, which offers a robust and reliable connection. Known as "stick and twist." Used where movement or vibrations might occur, and well suited for the outdoors, like wind, rain, and snow. Commonly used with MMF. ^4d8066

Mechanical Transfer-Registered Jack (MTRJ): Features a small, rectangular design and houses both the transmit and receive fibers in a single connector. Uses a latch mechanism like other RJ connectors. Having two fibers in one connector makes it good for dense environments. ^aea722

Multi-Fiber Push On (MPO): Designed to accommodate multiple fibers in a single connector, significantly increasing the capacity and flexibility of fiber networks. Usually 12 or more fibers in a single connector. Widely used in high-density data centers. Reduces installation time. ^c338d2

Back Reflection: When light reflects back into the transmitter, causing signal degradation. Affected by the type of polish used. ^4446d7

Physical Contact (PC): A polish with a slight curvature. Lower back reflection than a straight cut, but the least effective of the three polish types. Common in telephone services. Best for lower speeds or short distances. ^06fde8

Ultra Physical Contact (UPC): An updated version of PC with a dome-shaped end face. Lower back reflection than PC. Found in broadband, data, and video uses. Good balance between performance and cost. ^5a7d62

Angled Physical Contact (APC): A polish with an 8 degree angle. Least amount of back reflection. Often used in long-haul applications like undersea connections. Expensive. ^cc33bb
