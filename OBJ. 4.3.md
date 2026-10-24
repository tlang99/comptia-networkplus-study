### Network Access Control (NAC)

[[#^d529c1|Network Access Control (NAC)]] increases a network's security by inspecting each device when it first attempts to connect. Inspection uses:
* [[#^e59334|Port security]]
* [[#^5eace4|MAC filtering]]
* [[#^52fd64|802.1X authentication]]

### 802.1X

802.1X typically involves three components:
1. [[#^08729d|Supplicant]]: the user's device seeking access
2. [[#^1bd227|Authenticator]]: the network device the user wants to connect to
3. [[#^36048c|Authentication server]]: the server that authenticates the user's device, most commonly a [[#^e8de7d|RADIUS]] server

The authenticator acts like a gatekeeper, blocking all traffic except the 802.1X authentication traffic sent by the user's device.

802.1X is also how enterprise mode authenticates on wireless networks: see [[Wireless Security#^aee373|Wireless Security]].

### NAC Agents

There are two types of NAC agents:
* [[#^f02869|Persistent agent]]: installed on company-provided computers
* [[#^ca40bd|Non-persistent agent]]: a temporary agent for users' personally owned devices

Both agents check that the MAC address is on the approved list, then verify the device's identity using 802.1X. A device that fails either check is quarantined.

### Access Control Rules

NAC can also be tailored to other requirements:
* [[#^c6cf03|Time-based access control]]
* [[#^7bdac5|Location-based access control]]
* [[#^db6b6a|Role-based access control]]
* [[#^2701f4|Rule-based access control]]

If a device fails inspection, it's quarantined and stays there until it's fixed (remediated) and deemed trustworthy.

### Glossary

Network Access Control (NAC): A method of increasing a network's security by inspecting devices trying to connect to it. Each device presents itself for inspection when it first attempts to connect. ^d529c1

Port Security: Secures physical network ports to prevent unauthorized access. Ex. can be configured to allow only a set of MAC addresses on a port. ^e59334

MAC Filtering: Controls which devices can access the network based on their MAC addresses. Allowing only listed addresses is known as allow listing. Many devices also support block listing, which is considered less secure than allow listing. ^5eace4

802.1X Authentication: An authentication framework that ensures only authenticated users can access network services. Works by encapsulating EAP within frames, which allows authentication with passwords, smart cards, and certificates. ^52fd64

Supplicant: The user's device seeking to access the network. ^08729d

Authenticator: The network device the user wants to connect to. Acts as a gatekeeper, blocking all traffic except 802.1X authentication traffic. ^1bd227

Authentication Server: The server on the network that authenticates the user's device. Most commonly a RADIUS server. ^36048c

Remote Authentication Dial-In User Service (RADIUS): The most common type of authentication server used with 802.1X. ^e8de7d

Persistent Agent: A NAC agent installed on company-provided computers. ^f02869

Non-persistent Agent: A NAC agent for users' personally owned devices. Users connect to the network and reach a captive portal, which asks them to run a temporary agent that assesses the device's compliance and then removes itself. ^ca40bd

Time-Based Access Control: Limits a device's network access to specified hours, based on the organization's operating times. ^c6cf03

Location-Based Access Control: Uses geolocation to verify the physical location of the device. ^7bdac5

Role-Based Access Control: Provides or limits access based on the user's role in the organization. ^db6b6a

Rule-Based Access Control: Uses a set of predefined rules to grant or deny access based on logical conditions. ^2701f4
