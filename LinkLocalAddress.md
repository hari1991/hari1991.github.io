In computer networking, a link-local address is a network address that is valid only for communications on a local link, i.e. within a subnetwork that a host is connected to. Link-local addresses are typically assigned automatically through a process known as link-local address autoconfiguration,[1] also known as auto-IP, automatic private IP addressing (APIPA, specific to IPv4), and stateless address autoconfiguration (SLAAC, specific to IPv6). While most link-local addresses are unicast, this is not necessarily the case; e.g. IPv6 addresses beginning with ff02: (ff02::/16), and IPv4 addresses beginning with 224.0.0. (224.0.0.0/24) are multicast addresses that are link-local.

Link-local addresses are not guaranteed to be unique beyond their network segment. Therefore, routers do not forward packets with link-local source or destination addresses.

IPv4 link-local unicast addresses are assigned from address block 169.254.0.0/16 (169.254.0.0 through 169.254.255.255). In IPv6, unicast link-local addresses are assigned from the block fe80::/10.

The Internet Engineering Task Force (IETF) has reserved the IPv4 address block 169.254.0.0/16 (169.254.0.0 – 169.254.255.255) for link-local addressing.[1] The entire range may be used for this purpose, except for the first 256 and last 256 addresses (169.254.0.0/24 and 169.254.255.0/24), which are reserved for future use and must not be selected by a host using this dynamic configuration mechanism.[1]: 2.1  Link-local addresses are assigned to interfaces by host-internal, i.e. stateless, address autoconfiguration when other means of address assignment are not available.

The simultaneous use of IPv4 addresses of different scope on the same interface, such as configuring link-local addresses as well as globally routable addresses, may lead to confusion and increased complexity.[1]: 1.9  Therefore, hosts search for a DHCP server on the network before assigning link-local addresses.

In the automatic address configuration process, network hosts select a random candidate address within the reserved range and use Address Resolution Protocol (ARP) probes to ascertain that the address is not in use on the network. If a reply is received to the ARP probe, it indicates the candidate IP address is already in use; a new random candidate IP address is then created and the process repeated. The process ends when there is no reply to the ARP, indicating the candidate IP address is available.

When a globally routable or a private address becomes available after a link-local address has been assigned, the use of the new address should generally be preferred to the link-local address for new connections but communication via the link-local address is still possible.[1]: 2.6.1 

Microsoft refers to this address autoconfiguration method as Automatic Private IP Addressing (APIPA).
