### Web Ports and Protocols

Two main ports are used for the web:
* Port 80: [[#^425a73|HTTP]]
* Port 443: [[#^f796a6|HTTPS]]

### Email Ports and Protocols

Email communication involves three main protocols. SMTP sends mail, while POP3 and IMAP retrieve it:
* [[#^b4c5d6|SMTP]]: Port 25 (SMTPS: 465 and/or 587)
* [[#^c5d6e7|POP3]]: Port 110
* [[#^d6e7f8|IMAP]]: Port 143 (IMAPS: 993)

### File Transfer Ports and Protocols

File transfer uses the following main protocols:
* [[#^e7f809|FTP]]: Ports 20 and 21
* [[#^f8091a|SFTP]]: Port 22
* [[#^091a2b|TFTP]]: Port 69
* [[#^1a2b3c|SMB]]: Port 445

### Glossary

Hypertext Transfer Protocol (HTTP): An Application Layer (Layer 7) protocol that enables plain text communication between clients and servers. HTTP is not encrypted and sends data in plain text. It has largely been replaced by HTTPS. Uses port 80. ^425a73

Hypertext Transfer Protocol Secure (HTTPS): Improved version of HTTP that adds a layer of security by encrypting data between the client and the server. It does this via either [[#^a3b4c5|SSL]] or [[#^92a3b4|TLS]], primarily SSL. Uses port 443. HTTPS should always be used over HTTP for the added security. Over 95% of web traffic now uses HTTPS. ^f796a6

Transport Layer Security (TLS):  ^92a3b4

Secure Sockets Layer (SSL):  ^a3b4c5

Simple Mail Transfer Protocol (SMTP): Standard protocol used for sending emails across the internet. Operates over port 25. Used only for OUTBOUND emails, not for receiving. Considered insecure, since emails are sent in plain text. SMTPS was introduced as a secure version of SMTP; it operates over port 465 and/or port 587 and encrypts messages. ^b4c5d6

Post Office Protocol version 3 (POP3): Used to retrieve emails from a remote server to a local client over port 110. It deletes the messages from the email server once they are downloaded to the client. This means you can only view your messages on the first device that downloaded them, not on multiple devices. It is an insecure protocol. POP3S was introduced as a secure variant. ^c5d6e7

Internet Message Access Protocol (IMAP): Operates on port 143. Allows users to manage emails directly on the email server, which makes it useful for viewing emails on multiple devices. It is also insecure. IMAPS, which operates over port 993, is the secure version and encrypts email. ^d6e7f8

File Transfer Protocol (FTP): Used to transfer files between a client and a server over a network. Uses two ports: port 20 for the actual data transfer and port 21 for sending control commands. Insecure and unencrypted. ^e7f809

Secure File Transfer Protocol (SFTP) / SSH File Transfer Protocol: Created to address the security concerns of FTP. Operates over port 22. Works by tunneling FTP through an SSH connection, which is already encrypted. ^f8091a

Trivial File Transfer Protocol (TFTP): Operates on port 69. A more basic version of FTP, designed for sending files when minimal security is sufficient. ^091a2b

Server Message Block (SMB): Operates on port 445. Allows computer apps to read and write to files and request services from server programs, letting Windows computers share files over a network. Used inside LANs, not for sending data across the internet like FTP or SFTP. ^1a2b3c
