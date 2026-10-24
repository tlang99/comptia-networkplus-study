### Spanning Tree Protocol

[[#^8e03ca|Spanning Tree Protocol (STP)]] permits redundant links between switches while preventing traffic from looping. Without STP, loops cause [[#^4caddc|broadcast storms]].

STP elects one switch as the reference point and gives every port a role:
* [[#^089e80|Root bridge]]: the switch with the lowest [[#^c13606|bridge ID]]
* [[#^b056b5|Non-root bridge]]: every other switch
* [[#^80d5aa|Root port]]: each non-root bridge's one port closest to the root bridge
* [[#^fdea02|Designated port]]: each segment's port closest to the root bridge. Every port on the root bridge is designated.
* [[#^000553|Non-designated port]]: blocks traffic to keep the topology loop-free

"Closest" is measured in [[#^3f6efa|link cost]], not distance.

NOTE: Dion says to remember for the exam: a lower speed has a higher cost, and a higher speed has a lower cost.

### Port States

If a link goes down, a non-designated port can move into a forwarding state and become a designated or root port. It goes through four states to get there:
1. Blocking: [[#^0cb611|BPDUs]] are received but not forwarded
2. Listening: processes BPDUs, and the switch determines its role in the spanning tree
3. Learning: populates the MAC address table, but doesn't forward frames yet
4. Forwarding: forwards frames for normal operation

### Glossary

Spanning Tree Protocol (STP): Also known as 802.1D. Permits redundant links between switches and prevents looping of network traffic. Works by electing a root bridge and assigning a role to every port. ^8e03ca

Bridge ID: Made up of a priority value and a MAC address. The lowest bridge ID becomes the root bridge. ^c13606

Root Bridge: The switch with the lowest bridge ID, elected as the reference point for the spanning tree. ^089e80

Non-root Bridge: Every switch other than the root bridge. ^b056b5

Root Port: Every non-root bridge has a single root port, the port closest to the root bridge in terms of cost. Faster cables have lower cost and slower cables have higher cost. If all cables are the same, the lowest port number is chosen. ^80d5aa

Designated Port: Every network segment has a designated port, the port on that segment closest to the root bridge in terms of cost. All ports on the root bridge are designated ports. ^fdea02

Non-designated Port: A port that blocks traffic to create a loop-free topology. Still receives BPDUs. If a link in the topology goes down, it can determine whether it needs to move to a forwarding state and become a designated port or root port. ^000553

Bridge Protocol Data Unit (BPDU): The messages switches exchange in STP. Non-designated ports keep receiving them while blocking. ^0cb611

Link Cost: Associated with the speed of a link. The lower the link's speed, the higher the cost. ^3f6efa

Broadcast Storm: Multiple copies of frames being forwarded back and forth until they consume the network. ^4caddc
