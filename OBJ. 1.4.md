### Ports and Protocols

Every network service follows a [[#^2b3c4d|protocol]] and communicates through a [[#^1a2f3e|port]]. Ports are numbered from 0 to 65,535 and are broken down into 3 categories:
* Well-known Ports: 0 to 1,023. Includes FTP on ports 20 and 21, SMTP on port 25, web browsing on 80, and secure web browsing on 443.
* Registered Ports: 1,024 to 49,151. Both these and well-known ports are registered with the Internet Assigned Numbers Authority (IANA).
* Ephemeral Ports: 49,152 to 65,535. Short-lived, temporary ports that can be used at any time without needing to request permission like the ports above. Closed once data transfer is complete.

The protocols for this objective are split into three notes:
* [[TCP, UDP, and ICMP]]
* [[Web, Email, and File Transfer Protocols]]
* [[Remote Access and Network Service Protocols]]

### Port Quick Reference

| Port | Protocol | TCP/UDP |
| --- | --- | --- |
| 20, 21 | FTP (20 data, 21 control) | |
| 22 | SSH, SFTP | |
| 23 | Telnet | |
| 25 | SMTP | |
| 53 | DNS | TCP and UDP |
| 67, 68 | DHCP (67 server listens, 68 client receives) | UDP |
| 69 | TFTP | |
| 80 | HTTP | |
| 110 | POP3 | |
| 123 | NTP | UDP |
| 143 | IMAP | |
| 161, 162 | SNMP (161 manager to agent, 162 agent reports back) | |
| 389 | LDAP | TCP and UDP |
| 443 | HTTPS | |
| 445 | SMB | |
| 465, 587 | SMTPS | |
| 514 | Syslog | UDP by default, or TCP |
| 636 | LDAPS | TCP |
| 993 | IMAPS | |
| 1433 | Microsoft SQL | |
| 3306 | MySQL | |
| 3389 | RDP | TCP |
| 5060 | SIP | UDP and TCP |
| 5061 | SIP over TLS | TCP |

### Glossary

Port: Virtual entry/exit point for communications used by software applications to exchange information. A logical opening in a computer that represents a service or application. ^1a2f3e

Protocol: Set of rules and conventions for data exchange between network devices. ^2b3c4d
