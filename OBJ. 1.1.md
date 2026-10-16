### OSI Model (Open Systems Interconnection)

The [[#^8b2f4a|OSI Model]] was developed in 1977 by the International Organization for Standardization (ISO). [[#^3e6c91|ISO 7498]] is the standard that refers to the OSI model. It is also called the OSI reference model, and can be used across all devices, manufacturers, etc. As a [[#^f7a05b|Reference Model]], it is used during troubleshooting efforts.

The OSI Model has seven layers:
* [[Layer 1 (Physical Layer)|Layer 1: Physical]]
* [[Layer 2 (Data Link Layer)|Layer 2: Data Link]]
* [[Layer 3 (Network Layer)|Layer 3: Network]]
* [[Layer 4 (Transport Layer)|Layer 4: Transport]]
* [[Layer 5 (Session Layer)|Layer 5: Session]]
* [[Layer 6 (Presentation Layer)|Layer 6: Presentation]]
* [[Layer 7 (Application Layer)|Layer 7 (Top Layer): Application]]

Please (Physical) Do (Data Link) Not (Network) Throw (Transport) Sausage (Session) Pizza (Presentation) Away (Application)

Data is transported through the 7 layers of the model as a [[#^f58c03|Protocol Data Unit (PDU)]], which is named differently depending on the layer it is currently in:
* Data: Used for layers 5, 6, and 7
* Segment: Layer 4
* Packet: Layer 3
* Frame: Layer 2
* Bit: Layer 1

Do (Data) Some (Segment) People (Packet) Fear (Frame) Birthdays (Bit)

### Encapsulation and Decapsulation

[[#^c2586f|Encapsulation]] is the process of putting headers, and optionally trailers, around data. The reverse of this is [[#^d36981|decapsulation]], where these are stripped away to leave only the original data. When data is traveling DOWN the OSI model, it is encapsulated. When it moves UP, it is decapsulated.

When a user creates data, it is entered into an application at Layer 7. This data is then encapsulated within a Layer 7 header that contains specific metadata. As it moves down to Layer 6, it is encapsulated again, with Layer 6 adding its own header containing more specific metadata about that layer's services. This continues all the way down to Layer 1.

The headers added at Layers 4, 3, 2, and 1 are very specific. At Layer 4, the header can be either a [[Layer 4 (Transport Layer)#^8e1a2b|TCP]] or a [[Layer 4 (Transport Layer)#^a03c4d|UDP]] header.

The TCP header is 20 bytes and contains:
* Source port
* Destination port
* Sequence number
* Acknowledgement number
* Offset
* Reserved
* TCP flags
* Window
* Checksum
* Urgent Pointer
* Optionally, mTCP

The UDP header is 8 bytes and contains:
* Source port
* Destination port
* Length
* Checksum

The IP header contains:
* Version
* Length
* Type of Service
* Total Length
* Identifier
* Flags
* Fragmented Offset
* Time to Live
* Protocol
* Header Checksum
* Source IP
* Destination IP
* Options and padding

The Ethernet header contains:
* Destination MAC address
* Source MAC address
* [[#^069d14|EtherType]]
* Optional VLAN tag

##### Summary

As data moves down the layers, it is encapsulated. As it moves up, it is decapsulated. At Layer 4, the source and destination ports are added to the header. At Layer 3, the source and destination IP addresses are added. At Layer 2, the source and destination MAC addresses are added. At Layer 1, the Layer 2 frames are transmitted in binary as 1s and 0s via the medium. Going the other way, for instance once a switch receives the data, it will construct a frame, read the destination and source MAC addresses, and then strip away those fields.

### Glossary

OSI Model (Open Systems Interconnection): Seven layer model developed in 1977 by the International Organization for Standardization (ISO). Also called the OSI reference model. ^8b2f4a

ISO 7498: The standard that refers to the OSI model. ^3e6c91

Reference Model: Used to categorize the functions of a network in the OSI Model during troubleshooting efforts. ^f7a05b

Protocol Data Unit (PDU): A single unit of information transmitted within a computer network. PDUs are named after their layer, such as L7PDU for a Layer 7 PDU and L5PDU for a Layer 5 PDU. They also have specialized names, as listed above. ^f58c03

Encapsulation: The process of putting headers, and optionally trailers, around data as it moves down the OSI model. ^c2586f

Decapsulation: The reverse of encapsulation. Headers and trailers are stripped away as data moves up the OSI model, leaving only the original data. ^d36981

EtherType: Used to indicate which protocol is encapsulated in the payload of the frame. ^069d14
