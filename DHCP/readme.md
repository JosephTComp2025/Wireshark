IPv4 DORA vs. IPv6 SLAAC/NDP

This artifact compares how IPv4 and IPv6 assign addresses.
IPv4 uses DHCP with the DORA sequence (Discover, Offer, Request, Acknowledge)
IPv6 often defaults to SLAAC opposed to SARR. SLAAC using ICMPv6 Neighbor Discovery (Router Solicitation, Router Advertisement). DHCPv6 (SARR) exists but requires explicit server support, not seen in this lab.

IPV4:
Packet 17 is a DHCP Discover packet sent from 0.0.0.0 since it doesnt have an IP at the moment and it is sent to 255.255.255.255
Packet 18 is a DHCP Offer packet sent from 192.168.74.1 to 192.168.64.5
Packet 19 is a DHCP Request packet sent from the client 0.0.0.0 to 255.255.255.255
Packet 20 is a DHCP Ack packet from 192.168.74.1 to 192.168.64.5

IPV6:
Packet 21 is a ICMPv6 Neighbor Solicitation where the host generates a link-local address fe80::1498:77ff:fe23:7d64
Packet 23 is a ICMPv6 Neighbor Advertisement that has the router flag set which makes it an advertisement from router
packet 25 is a ICMPv6 Neighbor Solicitation 
Packet 26 is a ICMPv6 Neighbor Advetisement that has the router flag not set which make it an adverisement from host

This shows how IPv6 NDP distinguishes routers from hosts. Analysts can use these flags to detect rogue Router Advertisements — a common attack vector in IPv6 networks.

Analysis from the comparison between the IPv4 and IPv6:
IPv4: Centralized DHCP server controls address assignment 
IPV6: Router advertises prefix and gateway, client configures itself.

Detection Relevance:
Rogue DHCP servers (IPv4) or malicious Router Advertisements (IPv6) can disrupt connectivity.  
This case file demonstrates lifecycle awareness across both protocols.
