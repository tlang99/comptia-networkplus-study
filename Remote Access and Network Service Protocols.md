### Remote Access Ports and Protocols

The main remote access protocols are:
* [[#^2b3c4e|SSH]]: Port 22
* [[#^3c4d5f|Telnet]]: Port 23
* [[#^4d5e60|RDP]]: Port 3389

### Network Service Ports and Protocols

Key network service protocols:
* [[#^5e6f71|DNS]]: Port 53
* [[#^6f7082|DHCP]]: Ports 67 and 68
* [[#^708193|SQL Services]]: Varies by vendor (Microsoft SQL 1433, MySQL 3306)
* [[#^8192a4|SNMP]]: Ports 161 and 162
* [[#^92a3b5|Syslog]]: Port 514

### Other Network Service Ports and Protocols

* [[#^a3b4c6|NTP]]: Port 123
* [[#^b4c5d7|SIP]]: Ports 5060 and 5061
* [[#^c5d6e8|LDAP]]: Port 389 (LDAPS: 636)

### Glossary

Secure Shell (SSH): Protocol used for secure remote login and other secure network services over an unsecure network. Operates on port 22. Offers strong authentication and encryption, creating a secure, encrypted tunnel to execute text-based commands on a remote server. ^2b3c4e

Telnet: Operates over port 23. The oldest remote access protocol, it allows a user on one computer to log in remotely to another computer. Typically should only be used over a LAN. Insecure and lacks encryption. SSH was developed as the replacement for Telnet, and Telnet should not be used in modern times. ^3c4d5f

Remote Desktop Protocol (RDP): Proprietary protocol developed by Microsoft that gives users a GUI to connect to another computer over a network connection. Operates over port 3389 using TCP. Allows for encryption, smart card authentication, and bandwidth reduction mechanisms. ^4d5e60

Domain Name System (DNS): Translates human-readable domain names into IP addresses that computers can use to identify each other on a network. Uses port 53 by default and operates on both TCP and UDP: UDP for small messages, TCP for larger messages. ^5e6f71

Dynamic Host Configuration Protocol (DHCP): Used to automate the assignment of IP addresses, subnet masks, gateways, and other networking parameters to a client device. Listens for client requests over port 67, and clients receive responses back on port 68, using UDP. ^6f7082

SQL Services: Protocols used by database servers to manage queries and control operations from the client applications requesting them. There is no one dedicated port, as different vendors use different ports. The two most common are Microsoft SQL on port 1433 and MySQL on port 3306. ^708193

Simple Network Management Protocol (SNMP): Used for collecting information from and configuring network devices like servers, printers, hubs, switches, and routers over a network. Operates on two ports: port 161 is used by SNMP managers communicating with agents, and port 162 is used by agents reporting back to the managers. ^8192a4

System Logging (Syslog): Standard protocol for message logging that allows devices to send event messages across the network to an event message collector known as a Syslog server. Operates on port 514 using UDP or TCP depending on how it's configured. Uses UDP by default. ^92a3b5

Network Time Protocol (NTP): Used to synchronize the clocks of computers over a network, allowing networks to maintain accurate time. Operates on port 123 using UDP. ^a3b4c6

Session Initiation Protocol (SIP): Used for initiating, maintaining, and terminating real-time sessions that involve voice, video, messaging, and other communication services. Uses port 5060 over UDP and TCP, and port 5061 over TCP for encrypted signaling with TLS. ^b4c5d7

Lightweight Directory Access Protocol (LDAP): Protocol for accessing and maintaining distributed directory information services over a network. Uses port 389 over TCP and UDP. LDAP is insecure and unencrypted. LDAPS, or LDAP over SSL, is the newer, encrypted version and uses port 636 over TCP. ^c5d6e8
