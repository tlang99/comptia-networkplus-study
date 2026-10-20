### Physical Installations

This objective covers the important factors of physical installations:
* [[#^f0afbb|Cable distribution systems]]: wall jacks, patch panels, MDFs, IDFs, and other smaller key pieces
* Wiring a network and testing a network
* [[#Power Distribution Systems|Power distribution systems]]
* [[#^6cdb5b|HVAC]]
* [[#Fire Suppression Systems|Fire suppression systems]]

### Cable Distribution Systems

A [[#^f0afbb|cable distribution system]] connects the network's backbone in the MDF to the IDFs, and out to the end users' wall jacks. It consists of:
* [[#^5d0892|Demarcation point]]
* [[#^9b854c|Main distribution frame (MDF)]]
* [[#^6680d7|Intermediate distribution frame (IDF)]]
* [[#^d1f721|Racks]]
* [[#^d4ed30|Patch panels]]
* [[#^9e7a9c|Fiber distribution panels]]

A cable distribution system typically starts at the MDF, where the backbone switch resides. In small offices, everything can connect back to this one switch. Larger offices need more switches, called edge switches, placed in IDFs. Ex. floors 2 and 3 each have an IDF, every device on those floors connects to its floor's IDF, and each IDF connects back to the MDF.

Cables run between these points using [[#^a91509|cable trays]].

Racks come in multiple form factors:
* [[#^87cb10|2-post rack]]
* [[#^7d867b|4-post rack]]
* [[#^ff215b|Wall-mounted rack]]
* [[#^b55614|Full cabinet rack (rack enclosure)]]

Patch panels have two sides:
* Front side: network jacks, typically RJ-45
* Back side: a [[#^6fae5c|110 punchdown block]]

Always connect a wall jack's cable into a patch panel.

### Power Distribution Systems

Power distribution systems ensure consistent, reliable power delivery for network equipment. They cover:
* [[#^263b6c|Uninterruptible Power Supply (UPS)]]
* [[#^69aae1|Power Distribution Unit (PDU)]]
* [[#^efe395|Generator]]
* Managing power loads: important for preventing circuit overloads. Proper management means making sure no single circuit is under an excessive load, which could lead to outages or damage.
* Understanding [[#^4bf756|voltage]] considerations: equipment must operate properly for its region. Europe uses a 230 volt standard and the US uses 120 volts. Plugging a 230 volt power supply into a 120 volt piece of hardware can cause damage. Most devices today are dual voltage and can run on either, but it must still be considered.

### HVAC Systems

[[#^6cdb5b|HVAC]] provides:
* Temperature control: network equipment can generate large amounts of heat, and without HVAC, devices can overheat
* Humidity management: too much humidity leads to condensation, which damages equipment. Too little leads to static electrical charges.
* Airflow regulation: most data centers arrange racks in alternating rows of cold and hot air, and devices use [[#^3f94fb|port-side exhaust or intake]] airflow to match that layout

### Fire Suppression Systems

There are three types of fire suppression systems:
* [[#^d2e5ed|Wet pipe system]]: should really be avoided in data centers
* [[#^1df1c0|Pre-action system]]: still not great, since it uses water in a data center
* [[#^b2ea71|Special suppression system]]: uses a clean agent instead of water

### Glossary

Cable Distribution System: An organized system of network media that ensures efficient and reliable data communication. Consists of cables, wall jacks, patch panels, main distribution frames, intermediate distribution frames, and smaller key pieces. ^f0afbb

Demarcation Point: The location where the ISP's connection ends and the organization's network infrastructure and cabling begin. The ISP is responsible for maintaining the network up to this point. ^5d0892

Main Distribution Frame (MDF): Usually located in the same place as the demarcation point. Serves as the main starting point for all interior cabling distributed throughout the facility. Think of it like the trunk of a tree: the MDF is the trunk, and the intermediate distribution frames are the branches. The main point of presence router and the backbone switch are found here, and everything in the network connects back to this switch. In large organizations, the backbone switch may connect to smaller edge switches in each IDF, which connect back to the backbone switch. ^9b854c

Intermediate Distribution Frame (IDF):  ^6680d7

Cable Tray: A unit or assembly that secures cables, and the raceways used by the cables, as they run across the building. ^a91509

Racks: Sturdy frames designed to hold devices like switches, routers, patch panels, and servers to manage space efficiently. Come in multiple form factors. ^d1f721

2-post Rack: Has 2 vertical posts. Used for lighter equipment, or for patch panels and network cabling in telecommunications setups. ^87cb10

4-post Rack: Has 4 vertical posts. Offers more stability and support, ideal for heavier equipment. ^7d867b

Wall-mounted Rack: A space-saving solution for smaller equipment. Good for limited floor space. ^ff215b

Full Cabinet Rack (Rack Enclosure): A fully enclosed rack with sides and a door. Secure, and can have a lock installed. Good for high-value equipment. ^b55614

Patch Panel: A device with a number of jacks, used for connecting and routing cables in a convenient manner. Usually used to keep the server room better organized. The front side has network jacks (typically RJ-45), and the back side has a 110 punchdown block. ^d4ed30

110 Block: A type of punchdown block used for voice and data applications in copper-based networks. Twisted pair cables are terminated onto the block using a punchdown tool, which pushes the wiring down into the teeth of the block. ^6fae5c

Fiber Distribution Panel: Uses fiber connectors like SC, LC, ST, and MTRJ. There's no punchdown on the back. Can also act as a converter if needed, Ex. converting SC to LC. ^9e7a9c

Uninterruptible Power Supply (UPS): A device that provides emergency power to a load when the main power source fails. Also protects against surges and spikes in power. Good for short-duration power outages, since its battery life is relatively short. A good practice is to place one UPS at the bottom of each rack. ^263b6c

Power Distribution Unit (PDU): A device used to distribute electric power to various network devices. Designed to provide protection from surges, spikes, and brownouts. Not designed to supply power like a UPS. ^69aae1

Generator: Installed outside a data center to provide longer-term power during a power outage. ^efe395

Voltage: Electric potential difference. ^4bf756

HVAC: Technology used for indoor environment control. Provides temperature control, humidity management, and airflow regulation. ^6cdb5b

Port-side Exhaust and Intake: The direction air flows through a network device like a switch. Port-side exhaust pulls cool air in from the back and blows hot air out the side with the ports. Port-side intake pulls air in from the port side and exhausts it out the back. Devices are chosen so their airflow matches the data center's layout of alternating cold and hot rows. ^3f94fb

Wet Pipe System: A basic system that uses sprinklers and pipes that always contain water. A valve opens and releases water when the fire alarm goes off. Should really be avoided in data centers. ^d2e5ed

Pre-action System: Similar to a wet pipe system, but helps minimize the risk of accidental releases. Still not great, since it uses water in a data center. ^1df1c0

Special Suppression System: Uses a clean agent as part of its suppression system instead of water, like a gas that displaces oxygen. Must be used with an alarm so people know to evacuate, since it can be dangerous for employees. ^b2ea71
