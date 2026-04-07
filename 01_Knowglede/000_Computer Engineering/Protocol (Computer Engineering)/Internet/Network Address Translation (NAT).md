Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[Internet]],

---
## History
[[Internet Protocol version 4 (IPv4)]] uses 32-bit addresses, capable of uniquely addressing about 4.3 billion devices on the network. By 1992, it became evident that that would not be enough. 
The 1994 RFC 1631 describes NAT as a "short-term solution" to the two most compelling problems facing the Internet Protocol at that time: IP address depletion and scaling in routing. By 2004, NAT had become widespread.

![[NAT_1.jpg]]
The primary benefit of one-to-many NAT is mitigation of [wiki/IPv4 address exhaustion](https://en.wikipedia.org/wiki/IPv4_address_exhaustion "IPv4 address exhaustion") by allowing entire networks to be connected to the Internet using a single public IP address.
RFC 2663 uses the term **network address and port translation** (**NAPT**) for this type of NAT.

## Method
RFC 3489 specified the protocol _Simple Traversal of UDP over NATs_ ([STUN](https://en.wikipedia.org/wiki/STUN "STUN"))
- Endpoint-Independent NAT, Full Cone NAT, or NAT 1
- Address-Dependent NAT, Restricted Cone NAT, or NAT 2
- Address- and Port-Dependent NAT, Port Restricted Cone NAT, or NAT 3
- Address- and Port-Dependent NAT, Symmetric NAT, or NAT 4


## NAT Traversal
[[NAT traversal]] problems arise when peers behind different NATs try to communicate. One way to solve this problem is to use [port forwarding](https://en.wikipedia.org/wiki/Port_forwarding "Port forwarding"). Another way is to use various NAT traversal techniques. The most popular technique for TCP NAT traversal is [TCP hole punching](https://en.wikipedia.org/wiki/TCP_hole_punching "TCP hole punching").


## NAT in [[Internet Protocol version 6 (IPv6)|IPv6]]
Network address translation is not commonly used in IPv6 because one of the design goals of IPv6 is to restore end-to-end network connectivity. [ref](https://en.wikipedia.org/wiki/Network_address_translation#cite_note-32)



---
# References
Official website:
Wikipedia: https://en.wikipedia.org/wiki/Network_address_translation
Youtube: