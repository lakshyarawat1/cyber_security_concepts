# Cisco networking basics

## Bandwidth And Throughput

- Bandwidth is the capacity of a medium to carry data.
- Digital bandwidth measures the amount of data that flows from one place to another in a given amount of time.
- Bandwidth is typically measured in no. of bits that can be sent across the media in a second. (Kbps / Mbps / Gbps).

- Throughput is a measure of transfer of bits across the media over a given amount of time.
- Latency refers to the amount of time including delays, for data to travel from one given point to another.
- In an internetwork or network with multiple segments, throuhgput cannot be faster than the slowest link of the path.

## Client and Server

### Client and Server Roles

- All computers connected to a network directly are considered as hosts.
- Hosts can send and recieve messages on network. In modern networks, computer hosts can act as a client, a server or both.
- The software installed on the computer determines the role of it in the network.
- Servers are hosts that have software installed which enable them to provide information, like email, web pages to other hosts on the network.
- Client hosts have software installed that enable them to request and display information provided by the server.


### Peer to Peer Networks

- It is possible for a computer to run both client and server software at the same time.
- This type  of networks are called peer-to-peer (P2P) networks.
- The main disadvantage of p2p networks is that the performance of a host can be slowed down as it is acting as a client and server both.

- Advantages of P2P networks include : 
    - Easy to set up.
    - Less complex
    - Lower cost 
    - Can be used for simple tasks.

- Disadvantages : 

    - No centralized admininstration
    - Not as secure
    - Not scalable
    - All devices may act as client and server which can slow down performance.


### Peer to Peer Applications

- A P2P Application uses hybrid system where resources sharing is decentralized, but the indexes that point to resource locations are stored in a centralized directory.
- Each peer accesses in an index server to get the location of a resource stored on another peer.


## Network Components

- The network infrastructure contains three categories of hardware components : 

    - End devices (like Laptop, Desktop, Tablet etc.)
    - Intermediate device (like Router, Switch, Firewall)
    - Network media (LAN Media, Wireless media etc. )

- Devices and media are physical components or hardware of the network.


### End Devices

- These devices form interface between the users and the underlying communication network.
- Some examples of end devices are :
    - Computers
    - Network printers
    - Security cameras
    - Telephones
    - Mobile devices

- An end devices is either a source or destination of a message transmitted over the network. 
- In order to uniquely identify hosts, adresses are assigned.


## ISP Connectivity

- ISP Interconnection : A router is required to securely connect to a computer to an ISP.

- Cable Connection : Typically offered by cable television service providers, the internet data signal is carried on the coaxial cable that delivers cable television.
 
- DSL (Digital Subscriber Line) provides a high bandwidth, always on, connection to the internet. It requires a special high-speed modem that seperates the DSL signal telephone  and provides an Ethernet connection to a host computer or LAN.

- More connectivity options are Cellular, Satellite and Dial-up Telephone.


## Wireless networks

### Types of wireless networks 

- Bluetooth
- Near-Field Communication (NFC) : Connect the cash register and the smart device. Uses em waves to communicate.
- GPS (Global Positioning System)
- Wifi


### Configurating mobile Wifi Connectivity

- Select settings, add network.
- Enter the network SSID, touch security and select the security type.
- Enter password and touch save.


### Bluetooth Pairing

- Bluetooth pairing occurs when two devices establish bluetooth connection to share resources.
- Two devices should be in discoverable mode, i.e. visible, so that they can be detected.
- It transmits following information when another bluetooth device requests it :

    - Name
    - Bluetooth class
    - Services that the device use
    - Technical information, like features and version

- During the pairing process, a personal identification number (PIN) may be requested to authenticate the pairing process.
- The PIN is stored using pairing services, so it does not have to be entered the next time when connecting to the same device.


## Home networks basics

- Small business and home routers are used for home networks.
- There are two types of ports in home routers :

    - Ethernet ports : These ports connect to the internal switch portion of the router. These ports are usually labelled "Ethernet" or "LAN". All devices connected to the switch ports are on same local network.

    - Internet ports : This port is used to connect to device to another network. The internet port connects the router to a different network than the ethernet port. This port is often used to connect to the cable or DSL modem in roder to access the internet.


### LAN Wireless Tech

- The wireless technologies most frequently used in home networks are in the unlicensed 2.4 GHz and 5 GHz frequency ranges.
- Bluetooth technology makes use of 2.4GHz band. It is limited, slow speed, short-range communication.
- Other tech that uses 2.4GHz and 5GHz bands are modern wireless LAN techs that conform to various IEEE 802.11 standards. 
- Unlike bluetooth, 802.11 devices transmit at a much higher speeds giving them more range and improved throughput.


### Wired Network Technologies

- Most commonly implemented wired technology is ethernet. Ethernet uses the suite of protocols that allows network devices to communicate in LAN.
- Directly connected devices use an Ethernet patch cable, usually unshielded cable. These cables can be purchased with the RJ-45 connectors installed with various lengths.


### Wireless network 

- The main organization responsible for creation of wireless technical standards is the Institute of Electrical and Electronic Engineers (IEEE).
- The IEEE 802.11 standard governs the WLAN environment.
- The network mode determines the type of tech that must be supported. For example, 802.11b, 802.11n or Mixed Mode.
- Network name or SSID used to identify the WLAN, All devices that wish to participate in the WLAN must have same SSID.
- Standard channel specifies the channel over which the communication will occur. By default, this is set to Auto to allow the Access Point(AP) to determine the best path.
- SSID Broadcast determines if the SSID will be broadcasted to all devices within range. By default, set to enabled.


### Setting up the home router

- Many wireless routers have automatic setup utility that can be configured to basic settings.
- To connect to the router using a wired connection, plug the cable into a port or interface except the one labelled "internet".
- The "internet" port should be plugged with the DSL or modem cable.
- The DSL connection will have a port of telephone type cable, usually a RJ-11 connector.


## Communication protocols

- The rules or protocols must be followed in order for the message to be successfully delivered and understood. Among the protocols that govern successful human communication are these : 
    - An identified sender and reciever
    - Agreed upon method of communicating 
    - Common language and grammer
    - Speed and timing of delivery
    - Confirmation or acknowledgement requirements

- There are two protocol models in networking : 

    - TCP / IP
    - OSI Model

## Network media 

- Data is transmitted over the network using network media.
- The types of network media are :

    - Copper
    - Fiber Optics
    - Wireless


### Common Network cables

- The three most common network cables are :

    - __Twisted Pair Cable__ : Ethernet usually use twisted pair cable to interconnect devices. Wires are grouped in pairs and twisted together to reduce interference.

    - __Coaxial Cable__ : Coaxial cable is a kind of solid copper cable used to cable TV connection. Core is typically surrounded by a layer of insulation, braided metal shielding, and a protective jacket. It is used as a high-frequency transmission line to carry high-frequency or broadband signals

    - __Fiber-Optics Cable__ : They have a very high bandwidth, which enables them to carry very large amount of data. 


## Access Layer

### Encapsulation

- The process of placing one message format (the letter) inside another message format (the envelope) is called encapsulation.
- De-encapsulation occurs when the process is reversed by the recipient and the letter is removed from the envelope.
- Each computer message is encapsulated is a specific format, called a frame, before it is send across the network. 
- A frame acts as an envelope, it provides the address of the intended destination and the adress of the source host.

- The access layer provides the first line of networking devices that connect hosts to the network i.e. wired Ethernet.
- The ethernet switch is used at layer 2. When a host sends a message to another host connected to the same network, the switch accepts and decodes the frames to read the MAC address portion of the message.
- A switch maintains a MAC address table by examining the source MAC address of each frame that is sent between the hosts.
- The table is dynamically updated each time a new source MAC address is read by the switch.


## Internet Protocol

### IPv4 address

- The IPv4 address is a logical network address that identifies a particular host. It must be properly configured and unique within the LAN, for local communication.
- It must be properly configured and unique in a world, for remote connections.
- Every packet sent across the internet has a source and destination IPv4 address. This information is required by networking devices to ensure that information gets to destination and any replies are returned to source.
- IPv4 address are 32 bits in length. It is normally represented in octal values like this 192.168.1.1.

- The logical 32-bit IPv4 address is hierarchical and is made up of two parts, the network and the host.
- The subnet mask is used to identify the network on which the host is connected.


### Unicast 

- Unicast transmission refers to one device sending a message to another device in one-to-one communication.
- A unicast packet has a destination IP address that is a unicast address which goes to a single recipient.

### Broadcast

- Broadcast transmission refers to a device sending a message to all the devices on a network in one-to-all communication.
- A broadcast packet has a destination IP address with all ones in the host portion, or 32 one bits.
- A broadcast may be directed or limited. 
- A directed broadcast is sent to all hosts on a specific network.
- A limited broadcast sends the packet to 255.255.255.255 by default.

### Multicast

- Multicast transmission reduces traffic by allowing a host to send a single packet to a selected set of hosts that subscribe to a multicast group.
- A multicast packet is a packet with a destination IP address that is multicast address. IPv4 has reserved the 244.0.0.0 to 239.255.255.255 addresses as a multicast range.
- Each multicast group is represented by a single IP address. When the IPv4 host subscribes to a multicast group, the host processes packets addressed to this multicast address and the packets addressed to its uniquely allocated unicast address.

### Types of IP addresses

- Public IP addresses can be accessed from anywhere in the globe whereas private IP addresses can be accessed by one within the network.


### Special Use IP Addresses

- There are certain addresses, such as the network address and broadcast address, that cannot be assigned to hosts. There are special addresses that can be assigned to hosts, but with restrictions on how those hosts can interact within the network.

- Loopback Addresses : (127.0.0.0 /8 or 127.0.0.1 to 127.255.255.254) are more commonly identified as only 127.0.0.1.
- These are special addresses used by a host to direct traffic to itself.

- Link Local Address : (169.254.0.0 /16 or 169.254.0.1 to 169.254.255.254) are more commonly identified as the automatic private IP addresses (APIPA) or self-assigned addresses.
- They are used by windows client to self-configure in the event that the client cannot obtain the IP addressing through other methods.


## Legacy ClassFul addressing

- IPv4 Addressing were assigned using classful addressing as defined in RFC 790. 
- The RFC divided the unicast ranges into specific classes :

    - __Class A(0.0.0.0/8 to 127.0.0.0/8)__ : Designed to support extremely large networks with more than 16 million host addresses. Class A uses a fixed /8 prefix with the first octet to indicate the network address and the remaining three octets for host addresses.

    - __Class B(128.0.0.0 /16 to 191.255.0.0 /16)__ : Designed to support the needs  for moderate to large networks with up to approximately 65,000 host addresses.  It uses a fixed /16 prefix with the two high-order octets to indicate the network address and the remaining two indicates the host address.

    - __Class C(192.0.0.0 /24 to 223.255.255.0 /24)__ : Designed to support small networks with max 254 hosts. Class C used a fixed /24 prefix with the first three octets indicate the network address and the last octet indicate the host address.

    - __Other Classes__ : There are also class D mulitcast block containing 224.0.0.0 to 239.0.0.0 and Class E for experimental address block consisting of 240.0.0.0 to 255.0.0.0.


### Assignment of IP addresses

- Both IPv4 and IPv6 addresses are managed by the Internet assigned Numbers Authority (IANA).
- IANA manages and allocated blocks of IP addresses to the Regional Internet Registries (RIRs).
- The RIRs are responsible for allocating IP addresses to ISPs which provide IPv4 address blocks to organisations and smaller ISPs.


## Network Segmentation

### Broadcast domains

- Routers do not propogate broadcasts. When a router recieves a broadcast, it does not forward it out to other interfaces.
- Therefore, each router interface connects to a broadcast domain and broadcasts are only propogated within that specific domain.
- A broadcast domain is a logical division of a computer network, in which all nodes can reach each other by broadcast at the data link layer.
- A broadcast domain is an area where all devices on a network can send messages to each other without any restrictions.

### Problem with large broadcast domains

- A large broadcast domain in a network that connects any hosts. A problem with a large broadcast domain is that these hosts can generate excessive broadcasts and negatively affect the network.
- This results in slow network operations due to the significant amount of traffic it can cause, and slow device operations because a device must accept and process each request that is broadcasted.

- The solution is to reduce the size of the network to create smaller broadcast domains in a process called subnetting.
- These smaller network spaces are called subnets.


### Reason for segmenting networks

- Subnetting reduces overall network traffic and improves network performance. It enables the administrator to implement security policies such as which subnet are allowed or not allowed to communicate together.
- It reduces the amount of devices affected by abnormal broadcast traffic due to misconfiguration, hardware/software problems or malicious intent.


## IPv6

### Issues with IPv4

- IPv4 IP addresses are less in amount than demand.
- IPv4 has theoritically maximum 4.3 billion addresses. Private addresses in combination with Network Address Translation (NAT) have been instrumental in slowing the depletion of IPv4 addresses.
- However, NAT is problematic for many applications, creates latency, and has limitations that severely impede peer-to-peer communications.

### IPv4 and IPv6 co-existence

- The IETF has created various protocols and tools to help network admins migrate their networks to IPv6.
- The migration techniques can be divided into three categories :

    - Dual Stack : Dual stack allows Iv4 and IPv6 to coexist on the same network segment. Dual stack devices run both IPv4 and IPv6 protocols stack simultaneously. Known as native IPv6, this means the customer network has an IPv6 connection  to their ISP and is able to access content found on the internet over IPv6.

    - Tunneling : Tunneling is a method of transporting an IPv6 packet over an IPv4 network. IPv6 packet is encapsulated inside the IPv4 packet, similar to other types of data.

    - Translation : Network Address Translation 64(NAT 64) allows IPv6 enabled devices to communicate with IPv4 enabled devices using a translation technique similar to NAT for IPv4. IPv6 packet  is translated to an IPv4 packet and vice versa.


### IPv6 Addressing

- IPv6 addresses are 128 bits in length and written as a string of hexadecimel values. Every four bits is represented by a single hex digit; for a total of 32 hex values.
- IPv6 addresses are non case-sensitive.

- A hextet is an unofficial term used to refer to a segment of 16 bits, or four hex digits.
- Preffered format for IPv6 is using all 32 hexadecimal digits. It does not necessaryily mean that it is the ideal method for representing the IPv6 address.


### Rules for IPv6 Addressing

- Omit Leading Zeroes : This rule reduces the notation in any hextet. This rule omits all the leading zeroes in a hextet. The rule only applies to leading 0s, not trailing 0s, otherwise the address would be ambigious.