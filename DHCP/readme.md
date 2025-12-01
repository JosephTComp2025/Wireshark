IPv4 DORA vs. IPv6 SLAAC/NDP

This artifact compares how IPv4 and IPv6 assign addresses.
IPv4 uses DHCP with the DORA sequence (Discover, Offer, Request, Acknowledge)
IPv6 often defaults to SLAAC opposed to SARR. SLAAC using ICMPv6 Neighbor Discovery (Router Solicitation, Router Advertisement)

IPV4:
Packet 17 is a DHCP Discover packet sent from 0.0.0.0 since it doesnt have an IP at the moment and it is sent to 255.255.255.255
Packet 18 is a DHCP Offer packet sent from 192.168.74.1 to 192.168.64.5
Packet 19 is a DHCP Request packet sent from the client 0.0.0.0 to 255.255.255.255
Packet 20 is a DHCP Ack packet from 192.168.74.1 to 192.168.64.5

IPV6:
