# Networking Basics

## OSI Model

- Open Systems Interconnection (OSI) model is a conceptual model developed by ISO.
- Describes how communication should occur in a computer network.
- Has Seven layers

### Physical Layer (1)

- Deals with physical connection between devices
- This includes medium, and transmission.

### Data Link Layer (2)

- Represents the protocol that enables data transfer between nodes on the same network segment.
- Network segment refers to the group of networked devices using a shared medium or channel for information transfer.
- Every device has a MAC (Medium Access Control) address.
- MAC address is usually expressed in hexadecimal format with a colon separating each two hexadecimal digit. Three leftmost bytes identify the vendor.

### Network Layer (3)

- Network layer enables data transfer between devices on different networks.
- This layer handles logical addressing and routing.
- Some protocols include IP, ICMP, VPN protocols like IPSec and SSL/TLS VPN.

### Transport Layer (4)

- Enables end-to-end communication between running application on different hosts.
- Uses two protocols TCP and UDP

### Session Layer (5)

- Responsible for establishing, maintaining and synchronizing communication between applications running on different hosts.
- Network File System (NFS) and Remote Procedure Call (RPC) are in session layer.

### Presentation Layer (6)

- Ensures that data is delivered in a form the application layer can understand.
- Handles data encoding, compression, and encrpytion.

### Application Layer (7)

- Provides network services directly to end-user application.
- Protocols used are HTTP,FTP,DNS,POP3,SMTP and IMAP.

## TCP/IP Model

- Developed in 1970s by Dept of Defense (DoD).
- Includes 4 layers.
- Application Layer - Includes Application, Presentation and Session layers of OSI Model.
- Transport Layer - Solo
- Internet Layer - Network Layer of OSI Model.
- Link Layer - DataLink Layer of OSI Model.

## IP Addresses and Subnets

- IP address is a unique identifier for a device in a network and wider internet.
- IPv4 and IPv6 are two major types/versions.
- IPv4 has four octets i.e. 32 bits, for example, `192.168.1.1`
- 0 and 255 are reserved for network and broadcasting addresses, respectively.
- IPv4 has at max 4 billion unique IPv4 addresses.

### Private Addresses

- Cannot be reached from outside the network.
- For having a private IP, the router must have a public IP address and must support Network Address Translation (NAT).
- RFC 1918 defines three ranges for private IP addresses :
  - `10.0.0.0`-`10.255.255.255`(`10/8`) Class A.
  - `172.16.0.0`-`172.16.255.255`(`172.16/12`) Class B.
  - `192.168.0.0`-`192.168.255.255`(`192.168/16`) Class C.

### Subnetting

- An Ipv4 address has 32 bits divided into 4 octets, 8 bits each.
- Every IP address has two parts :
  - Network portion - Identifies the network
  - Host portion - identifies the device on that network.
- Subnets mask determines where the division occurs.

### Routing

Some routing algorithms are :

- OSPF - Open Shortest Path First
- EIGRP - Enhanced Interior Gateway Routing Protocol, Cisco proprietary routing protocol that calculates the cost associated with routes and choose one of them.
- BGP - Border Gateway protocol, primary protocol used by the internet.
- RIP - Routing Information Protocol, often used in small networks.

## TCP and UDP

- Two protocols used in the transport layer.

### UDP

- Stands for User Datagram Protocol.
- UDP is a simple connectionless protocol that operates at the transport layer.
- Connectionless means it doesnot need to establish a connection to deliver a packet.
- There is no confirmation sent back from the reciever that the message has been delivered making UDP less reliable.

### TCP

- Stands for Transmissin Control Protocol
- Connection oriented transport protocol, ensures reliability in data delivery.
- TCP establishes a connection using the three-way handshake.
- Two SYN flags and one ACK flags are used to establish a connection.

## NAT

- Stands for Network Address Translation
- Uses one public IP address to provide internet access to multiple private IP addresses.
