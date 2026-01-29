# DHCP Protocol

- DHCP stands for Dynamic Host Configuration Protocol.
- It is an application level protocol that relies on UDP.
- DHCP configures the network hosts and devices automatically.
- Server listens on port 67 and client sends on port 68.

## Working

- DHCP Discover - The client broadcasts a `DHCPDISCOVER` message seeking the local DHCP server if one exists.
- DHCP Offer - The server responds with `DHCPOFFER` message with IP address available for the client to accept.
- DHCP Request - Client responds with `DHCPREQUEST` message to indicate that it is accepted the offered IP.
- DHCP Acknowledge - Server responds with `DHCPACK` message to confirm that offered IP is not assigned to this client.
