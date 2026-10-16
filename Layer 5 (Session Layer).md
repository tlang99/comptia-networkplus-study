The Session Layer keeps conversations separate to prevent data from intermingling. It manages each session in three stages:
* [[#^39cfd6|Setting up]]
* [[#^4ad0e7|Maintaining]]
* [[#^5be1f8|Tearing down]]

Layer 5 protocols include [[#^6cf209|H.323]] and [[#^7d031a|NetBIOS]].

### Glossary

Session Setup: Done by checking user credentials, then assigning a number to the session to identify it. ^39cfd6

Session Maintenance: Where data transfers back and forth across the network. If there is a break in the connection, it will be re-established. Receipt of the data is also acknowledged here. ^4ad0e7

Session Teardown: Ending the session once the transfer is done or when the other party disconnects. It can be done manually or after communication has finished. ^5be1f8

H.323: Protocol used to set up, maintain, and tear down voice and video connections, used over RTP. ^6cf209

NetBIOS: Used to share files over a network. ^7d031a
