Tags: #SecondBrain 
Status: #open, #unprocessed
Related: [[Internet]], [[OSI model]]

---
# DHCP

## Overview

[Internet Protocol](https://en.wikipedia.org/wiki/Internet_Protocol "Internet Protocol") (IP) defines how devices communicate within and across local networks on the Internet. A DHCP server can manage IP settings for devices on its local network, e.g., by assigning IP addresses to those devices automatically and dynamically.

DHCP operates based on the [client–server model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model "Client–server model"). When a computer or other device connects to a network, the DHCP client software sends a DHCP [broadcast](https://en.wikipedia.org/wiki/Broadcasting_\(networking\) "Broadcasting (networking)") query requesting the necessary information. Any DHCP server on the network may service the request. The DHCP server manages a pool of IP addresses and information about client configuration parameters such as [default gateway](https://en.wikipedia.org/wiki/Default_gateway "Default gateway"), [domain name](https://en.wikipedia.org/wiki/Domain_name "Domain name"), the [name servers](https://en.wikipedia.org/wiki/Name_server "Name server"), and [time servers](https://en.wikipedia.org/wiki/Time_server "Time server"). On receiving a DHCP request, the DHCP server may respond with specific information for each client, as previously configured by an administrator, or with a specific address and any other information valid for the entire network and for the time period for which the allocation (_lease_) is valid. A DHCP client typically queries this information immediately after [booting](https://en.wikipedia.org/wiki/Booting "Booting"), and periodically thereafter before the expiration of the information. When a DHCP client refreshes an assignment, it initially requests the same parameter values, but the DHCP server may assign a new address based on the assignment policies set by administrators.

On large networks that consist of multiple links, a single DHCP server may service the entire network when aided by DHCP relay agents located on the interconnecting routers. Such agents relay messages between DHCP clients and DHCP servers located on different subnets.

Depending on implementation, the DHCP server may have three methods of allocating IP addresses:
**Dynamic allocation**
A [network administrator](https://en.wikipedia.org/wiki/Network_administrator "Network administrator") reserves a range of IP addresses for DHCP, and each DHCP client on the [LAN](https://en.wikipedia.org/wiki/LAN "LAN") is configured to request an IP address from the DHCP [server](https://en.wikipedia.org/wiki/Server_\(computing\) "Server (computing)") during network initialization. The request-and-grant process uses a lease concept with a controllable time period, allowing the DHCP server to reclaim and then reallocate IP addresses that are not renewed.

**Automatic allocation**
The DHCP server permanently assigns an IP address to a requesting client from a range defined by an administrator. This is like dynamic allocation, but the DHCP server keeps a table of past IP address assignments, so that it can preferentially assign to a client the same IP address that the client previously had.

**Manual allocation**
This method is also variously called _static DHCP allocation_, _fixed address allocation_, _reservation_, and _MAC/IP address binding_. An administrator maps a unique identifier (a _client id_ or [MAC address](https://en.wikipedia.org/wiki/MAC_address "MAC address")) for each client to an IP address, which is offered to the requesting client. DHCP servers may be configured to fall back to other methods if this fails.

DHCP services are used for [Internet Protocol version 4](https://en.wikipedia.org/wiki/Internet_Protocol_version_4 "Internet Protocol version 4") (IPv4) and [IPv6](https://en.wikipedia.org/wiki/IPv6 "IPv6"). The details of the protocol for IPv4 and IPv6 differ sufficiently that they may be considered separate protocols. For the IPv6 operation, devices may alternatively use stateless address autoconfiguration. IPv6 hosts may also use [link-local addressing](https://en.wikipedia.org/wiki/Link-local_addressing "Link-local addressing") to achieve operations restricted to the local network link.


## Example
OSI model:
	Application layer: DHCP --> Transport layer: UDP 
[Example capture by Wireshark](https://community.ruckuswireless.com/t5/RUCKUS-Self-Help/Understanding-DHCP-DORA-process-from-Wireshark-packet-capture/m-p/71576)


## Security
See also: [DHCP snooping](https://en.wikipedia.org/wiki/DHCP_snooping "DHCP snooping")

The base DHCP does not include any mechanism for authentication.  Because of this, it is vulnerable to a variety of attacks. These attacks fall into three main categories: 
- Unauthorized DHCP servers providing false information to clients.
- Unauthorized clients gaining access to resources.
- Resource exhaustion attacks from malicious DHCP clients.

## IETF standards documents

- [RFC 2131](https://www.rfc-editor.org/rfc/rfc2131) – "Dynamic Host Configuration Protocol,"
- [RFC 2132](https://www.rfc-editor.org/rfc/rfc2132) – "DHCP Options and BOOTP Vendor Extensions,"
- [RFC 3046](https://www.rfc-editor.org/rfc/rfc3046) – "DHCP Relay Agent Information Option,"
- [RFC 3203](https://www.rfc-editor.org/rfc/rfc3203) – "DHCP reconfigure extension,"
- [RFC 3397](https://www.rfc-editor.org/rfc/rfc3397) – "Dynamic Host Configuration Protocol (DHCP) Domain Search Option,"
- [RFC 3442](https://www.rfc-editor.org/rfc/rfc3442) – "The Classless Static Route Option for Dynamic Host Configuration Protocol (DHCP) version 4,"
- [RFC 3942](https://www.rfc-editor.org/rfc/rfc3942) – "Reclassifying Dynamic Host Configuration Protocol version 4 (DHCPv4) Options,"
- [RFC 4361](https://www.rfc-editor.org/rfc/rfc4361) – "Node-specific Client Identifiers for Dynamic Host Configuration Protocol Version Four (DHCPv4),"
- [RFC 4388](https://www.rfc-editor.org/rfc/rfc4388) – "Dynamic Host Configuration Protocol (DHCP) Leasequery,"
- [RFC 4436](https://www.rfc-editor.org/rfc/rfc4436) – "Detecting Network Attachment in IPv4 (DNAv4),"
- [RFC 6926](https://www.rfc-editor.org/rfc/rfc6926) – "DHCPv4 Bulk Leasequery,"
- [RFC 7724](https://www.rfc-editor.org/rfc/rfc7724) – "Active DHCPv4 Lease Query,"
- [RFC 8415](https://www.rfc-editor.org/rfc/rfc8415) – "Dynamic Host Configuration Protocol for IPv6 (DHCPv6),"






---
# References
Official website:
Wikipedia: https://en.wikipedia.org/wiki/Dynamic_Host_Configuration_Protocol
Youtube: