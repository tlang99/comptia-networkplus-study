Layer 4 serves as the dividing line between the lower layers (physical, data link, network) and the upper layers of the OSI model. Data at this layer is known as a Segment, or as a Datagram when using UDP.

Layer 4 contains two protocols, [[#^8e1a2b|TCP]] and [[#^a03c4d|UDP]]. It also includes two additional reliability features, [[#^b14d5e|Windowing]] and [[#^c25e6f|Buffering]].

TCP vs. UDP:
* TCP: Reliable, connection-oriented, segment retransmission and flow control through windowing, segment sequencing, acknowledges segments
* UDP: Unreliable, connectionless, no windowing or retransmission, no sequencing, does not acknowledge segments

Use TCP when it is vital that someone receives something. Use UDP when streaming things like audio or video.

TCP uses flags to manage its connections:
* [[#^d36f70|SYN]]
* [[#^e47a81|ACK]]
* [[#^f58b92|FIN]]
* [[#^069ca3|RST]]
* [[#^17adb4|PSH]]
* [[#^28bec5|URG]]

Layer 4 devices include WAN Accelerators, Load Balancers, and Firewalls (which can sometimes operate at Layer 4).

### Glossary

Transmission Control Protocol (TCP): Connection-oriented protocol that is a reliable way to transport segments across the network. TCP verifies that the recipient received a segment using the [[#^9f2b3c|three-way handshake]]. If it doesn't receive an acknowledgment, it resends the segment. ^8e1a2b

Three-Way Handshake: The client sends a [[#^d36f70|SYN]] packet to the server. When the server receives it, it sends a SYN-ACK packet back to the client. When the client receives that, it sends its own [[#^e47a81|ACK]] packet back to the server, completing the three-way handshake. The server will ask for retransmission if not all acknowledged segments were received. ^9f2b3c

SYN (Synchronization): Used to synchronize the connection during a three-way handshake. ^d36f70

ACK (Acknowledgement): Used during the three-way handshake, and also used to acknowledge the successful receipt of packets. ^e47a81

FIN (Finished): Used to tear down the virtual connections created by the three-way handshake and the SYN flag. ^f58b92

RST (Reset): Used when a client or server receives a packet that it was not expecting. ^069ca3

PSH (Push): Used to ensure the data is given priority and is processed at the sending or receiving ends. ^17adb4

URG (Urgent): Identifies incoming data as urgent. Unlike PSH, it tells the recipient that the data needs to be processed immediately and skip the queue. ^28bec5

User Datagram Protocol (UDP): Connectionless protocol that is an unreliable way to transport segments across the network. If a datagram is dropped, the sender is not made aware. However, it is very useful for media, since there is zero retransmission. It does not perform the three-way handshake that TCP does. ^a03c4d

Windowing: Allows clients to adjust the amount of data in each segment. More segments can be sent if no retransmissions are occurring, or fewer if many retransmissions are occurring. ^b14d5e

Buffering: Occurs when devices allocate memory to store segments if bandwidth is not readily available, then transmit them once it is. ^c25e6f
