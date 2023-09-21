# Computer Networks

A network is a set of connected devices.  
Network Topology refers to the layout of the computer network. The different topologies include - 
- Bus
- Ring
- Mesh
- Tree
- Hybrid

Network Reliability is characterised by multiple factors such as -
- Downtime
- Failure frequency
- Catastrophe
- Recovery Time

Some factors that affect the performance of a network include - 
- Number of users
- Harware and software
- Medium of transmission

## Types of Networks
- PAN (Personal Area Network) - Let devices connect and communicate over the range of a person. E.g. connecting Bluetooth devices.
- LAN (Local Area Network) - It is a privately owned network that operates within and nearby a single building like a home, office, or factory
- MAN (Metropolitan Area Network) - It connects and covers the whole city. E.g. TV Cable connection over the city
- WAN (Wide Area Network) - It spans a large geographical area, often a country or continent. The Internet is the largest WAN
- GAN (Global Area Network) - It is also known as the Internet which connects the globe using satellites. The Internet is also called the Network of WANs.

## VPN
VPN or the Virtual Private Network is a private WAN (Wide Area Network) built on the internet. It allows the creation of a secured tunnel (protected network) between different networks using the internet (public network). By using the VPN, a client can connect to the organization’s network remotely. VPN extends a private network across a public network.
Advantages of VPN include - 
- VPN is used to connect offices in different geographical locations remotely and is cheaper when compared to WAN connections.
- VPN is used for secure transactions and confidential data transfer between multiple offices located in different geographical locations.
- VPN keeps an organization’s information secured against any potential threats or intrusions by using virtualization.
- VPN encrypts the internet traffic and disguises the online identity.  
  

## Bandwidth
Bandwidth is the range of upper and lower limit frequencies alloted to a specific cause.
Bandwidth in networks refers to how much digital data we can send or receive through a link in a given length of time. It's also referred to as the data transfer rate. Bandwidth is basically a measure of the amount of data that can be sent and received at any instance of time. That simply means that the higher the bandwidth of a network, the larger the amount of data the network can be sending to and from across its path. Bandwidth is usually measured in bits transferred per second through a path or link. Common measures include bps, Mbps and Gbps. It is the bandwidth of a web page that determines how quickly it will load in a browser. It is a theoretical measure.  

Bandwidth can also refer to a range of frequencies.

## Speed, Latency and Throughput
- Speed tells how fast data is coming in while latency tells how late the information reaches user.
- Throughput - It is the determination of the amount of data is transmitted during a specified time period via a network, interface or channel. Also called as effective data rate or payload rate. 
  
  
## OSI Model
- Open System Interconnection
- It is called the OSI model as it deals with connecting the systems that are open for communication with other systems.
- 7 layers
- The layers are - Application, Presentation, Session, Transport, Network, Data Link, Physical
![OSI Model](Images\OSI.png)
### Physical Layer
- It is concerned with transmitting raw bits over a communication channel.
- Physical connection between devices
- Contains information in the form of bits
- Chooses which type of transmission mode is to be selected for the transmission. The available transmission modes are Simplex, Half Duplex and Full Duplex
- Data Unit - Bits
- Devices - Hubs, Modem, Cables
    - Hub - A hub has many ports in it. A computer which intends to be connected to the network is plugged in to one of these ports. When a data frame arrives at a port, it is broadcast to every other port, without considering whether it is destined for a particular destination or not. Hubs may be active(repeat and strengthen) or passive.
    - Modem - Modem stands for Modulator/Demodulator. The modem is defined as a networking device that is used to connect devices connected in the network to the internet. The main function of a modem is to convert the analog signals that come from telephone wire into a digital form.
    - Cable - To physically connect two devices. Some of the types of cables are coaxial cable, optical fiber cable, and twisted pair cable.
### Data Link Layer
- Ensures error-free data transfer
- Data Link layer is responsible to transfer data hop by hop (i.e within same LAN, from one device to another device) based on the MAC address. 
- It also allows detecting damaged packets using the CRC (Cyclic Redundancy Check) error-detecting, code.
- DLL encapsulates sender and receiver MAC addresses
- Functions include framing, error control and access control
- At the sender’s side, DLL receives packets from the Network layer and divides them into small frames, then, sends each frame bit-by-bit to the physical layer. It also attaches some special bits (for error control and addressing) at the header and end of the frame. At the receiver’s end, DLL takes bits from the Physical layer organizes them into the frame, and sends them to the Network layer. 
Data can get corrupted due to various reasons like noise, attenuation, etc. So, it is the responsibility of the data link layer, to detect the error in the transmitted data and correct it using error detection and correction techniques respectively. DLL adds error detection bits into the frame’s header, so that receiver can check received data is correct or not.
- When more than one node is connected to a shared link, Data Link Layer protocols are required to determine which device has control over the link at a given time.
- Data Unit - Frames
- Protocols - Synchronous Data Link Protocol (SDLC), High-Level Data Link Protocol (HDLC), Point to Point Protocol (PPP), Link Control Protocol (LCP), Network Control Protocol (NCP)
- Devices - Switch, NIC, Device Drivers
    - Switch - A switch is a data link layer networking device which connects devices in a network and uses packet switching to send and receive data over the network. when a data frame arrives at any port of a network switch, it examines the destination address and sends the frame to the corresponding device(s).
    - Network Interface Card - Network interface card is an electronic device that is mounted on ROM of the com that connects a computer to a computer network, usually a LAN.
    - Bridge - A bridge is a type of computer network device that provides interconnection with other networks that use the same protocol, connecting two different networks together and providing communication between them.
### Network Layer
- Transmission of data from one network to another
- Packet Routing - The network layer is responsible for creating routing table, and based on routing table, forwarding of the input request.
- Sender and receiver addresses are placed in the header
- It controls the operation of the subnet.
- The network layer takes care of feedback messaging through ICMP messages.
- If the packets are too large for delivery, they are fragmented i.e., broken down into smaller packets.
- Data Unit - Packets
- Devices - Routers 
    - Routers - A router is a switch like device that routes/forwards data packets based on their IP addresses. Routers normally connect Local Area Network (LANs) and Wide Area Network (WANs) together and have a dynamically updating routing table based on which they make decisions on routing the incoming packets.
### Transport Layer
- Responsible for end-to-end delivery of complete message
- The basic functionality of this layer is to accept data from the above layers, split it up into smaller units if needed, pass these to the network layer, and ensure that all the pieces arrive correctly at the other end.
- The Transport Layer takes care of Segmentation and Reassembly.
- Provides ack and re-transmits data if error
- Add source, destination port #
- To deliver the message to the correct process, the transport layer header includes a type of address called service point address or port address.
- Can be connection-oriented (establish connection, transfer data, disconnect) or connectionless
- Data Unit - Segments
- Protocols - Transmission Control Protocol (TCP), User Datagram Protocol (UDP)
### Session Layer
- Establishment of Connection
- Session maintenance
- Authentication and Security
- The session layer allows users on different machines to establish sessions between them.
- Data Unit - Message
- Protocols - Real-time Transport Control Protocol (RTCP), Point-to-Point Tunneling Protocol (PPTP), Password Authentication Protocol (PAP), Sockets Direct Protocol (SDP)
### Presentation Layer
- Data Translation, Encryption and Compression
- Translation: For example, ASCII to EBCDIC.
- Encryption/ Decryption: Data encryption translates the data into another form or code. The encrypted data is known as the ciphertext and the decrypted data is known as plain text. A key value is used for encrypting as well as decrypting data.
- Compression - Reduces the number of bits that need to be transmitted on the network.
- The presentation layer is concerned with the syntax and semantics of the information transmitted.
- It translates a message from a common form to the encoded format which will be understood by the receiver.
- Data Unit - Message
- Protocols - Lightweight Presentation Protocol (LPP), Secure Socket Layer (SLL)
### Application Layer
- Mail services, network virtual terminal
- Helps in identifying the client and synchronizing communication.
- Data Unit - Message
- Protocols - SMTP, DNS, TELNET, FTP

  
    

## TCP/IP Model
- Transmission Control Protocol / Internet Protocol
- It is a compressed version of the OSI model with only 4 layers. It was developed by the US Department of Defence (DoD) in the 1980s. 
- TCP does the work to send and receive data
- IP finds the destination
- 4 layers
- The layers are - Application, Transport, Internet, Link
### Link Layer
- Decides which links such as serial lines or classic Ethernet must be used to meet the needs of the connectionless internet layer
- Responsible for generating data, identify protocol type, framing, error prevention
- Physical + Data Link layer from OSI model
- Also called, Physical Layer or Network Interface Layer
### Internet Layer
- Route packets from one device to another
- It delivers the IP packets where they are supposed to be delivered.
- Also called Network layer
- Protocols - IP, ICMP, ARP
### Transport Layer
- Responsible for end-to-end delivery of complete message
- The basic functionality of this layer is to accept data from the above layers, split it up into smaller units if needed, pass these to the network layer, and ensure that all the pieces arrive correctly at the other end.
- Can be connectionless or connection-oriented
- Protocols - TCP, UDP
### Application Layer
- End-to-end communication
- User interaction
- High level protocols
- Application + Presentation + Session layers from OSI Model
- Protocols - HTTP, SSH  
  
    

## TCP/IP vs OSI Model
| TCP/IP | OSI |
|------------------------------|---------------------------------|
| Transmission Control Protocol/ Internet Protocol Model | Open System Interconnection Reference Model |
| 4 layers | 7 layers |
|Application, Transport, Network/Internet, Link Layers | Application, Presentation, Session, Transport, Network, Data Link, Physical Layers |
| More reliable | Less reliable |
| Developed Protocols first then model | Developed model first then protocols |
| Protocol Dependent | Protocol Independent |
| Connectionless communication in Network Layer | Connectionless and Connection-oriented communication in Network Layer |
| Internet implementation | Not implemented, only a reference model |
| Newer | Older |

## Networking Devices
| Hub | Switch | Router |
|------------------------------|-----------------------------|------------------------------------|
| Physical Layer | Data Link Layer | Network Layer |
| Repeats signal | Report and filter by MAC/LAN address | Route Data based on IP address |
| Connections within a single LAN | Connect multiple sub-LANS | Connect multiple LAN/WAN |


## Domain Name Server (DNS)
- It is used to locate a resource in a network
- DNS maps domain name to its IP address
- Top-level domain (TLD) server - It is responsible for com, org, edu, etc, and all top-level country domains like uk, fr, ca, in, etc. They have info about authoritative domain servers and know the names and IP addresses of each authoritative name server for the second-level domains. 

## Dynamic Host Configuration Protocol (DHCP)
- Dynamically assign IP address to new device in network
- When a new device enters a network, it broadcasts a message. The DHCP server respons to the message, other servers ignore the broadcasted message. The DHCP responds to new device and allocates an IP address.
- Discover, offer, acknowledge

## Network Interface Card
- NIC is used for laptops and other computing devices to provide wireless connection to LAN
- Every NIC has it's own MAC address to identify the device

## MAC Address
- Media Access Control address
- It is unique for each device
- 48 bit address

## IP Address
- IP address or Internet Protocol address is of two types, IPV4 and IPV6
- IPV4 is a 32 bit address, while IPV6 is 128 bits 
- IP address is the software address of the computer in the network
- Private Address - For each class, there are specific IPs that are reserved specifically for private use only. This IP address cannot be used for devices on the Internet as they are non-routable.  

### IPv4
The fourth and initially widely used version of the Internet Protocol is called IPv4 (Internet Protocol version 4). It is the most popular version of the Internet Protocol and is in charge of distributing data packets throughout the network. Maximum unique addresses for IPv4 is close to 4.3 billion, which is possible due to the use of 32-bit addresses. The network address and the host address are the two components of each address. The host address identifies a particular device within the network, whereas the network address identifies the network to which the host belongs. In the “dotted decimal” notation, which is the standard for IPv4 addresses, each octet (8 bits) of the address is represented by its decimal value and separated by a dot (e.g. 192.168.1.1). An IPv4 address has 4 octets of 8-bit each with each number with a value up to 255.
![Network Classes](Images\NetworkClasses.png)

### IPv6
The most recent version of the Internet Protocol, IPv6, was created to address the IPv4 protocol’s drawbacks. A maximum of 4.3 billion unique addresses are possible with IPv4’s 32-bit addresses. Contrarily, IPv6 uses 128-bit addresses, which enable a significantly greater number of unique addresses. This is significant because IPv4 addresses were running out and there are an increasing number of devices that require internet access. Additionally, IPv6 offers enhanced security features like integrated authentication and encryption as well as better support for mobile devices. IPv6 support has spread among websites and internet service providers, and it is anticipated to gradually displace IPv4 as the main internet protocol.

## MAC va IP Address
| MAC | IP |
| ------------------------------ | ------------------------------|
| Media Access Control Address	| Internet Protocol Address |
| 48 bit |	32 (IPv4) or 128 (IPv6) Byte address |
| It is embedded with NIC	| It is obtained from the network |
| Physical Address	| Logical Address |
| Operates at Data Link Layer |	Operates at Network Layer. |
| Helps to identify the device	| Helps to identify the device connectivity on the network |


## Subnetting
When a bigger network is divided into smaller networks, to maintain security, then that is known as Subnetting. Subnetting helps to organize and also structure the network in a certain way to reduce and manage traffic. Subnetting will help to lessen or disperse the pressure that the networks' heavy load causes. It also provides more security.  
For communicating between subnets, routers are used. Each subnet allows its linked devices to communicate with each other.

Subnetting is a technique for creating logical sub-networks from a single physical network (subnets). A company can grow its network via subnetting without asking for a new network number from its ISP. Subnetting hides network complexity while assisting in the reduction of network traffic. 

A subnet mask is a 32-bit number used to distinguish the network and host portions of an IP address.
If 12 subnets are needed, mask would be 255.255.255.240 (binary of 240 = 11110000)
Number of subnets = 2^(number of 1 bits) - 2 = 2^4 - 2 = 14
Number of hosts =  2^(number of 0 bits) - 2 = 2^4 - 2 = 14


## Protocol
A protocol is a set of rules to govern communication of information. Both the sender and receiver should follow the same protocols in order to communicate the data.

The internet and many other data networks work by organizing data into small pieces called packets. Each large data sent between two network devices is divided into smaller packets by the underlying hardware and software. Each network protocol defines the rules for how its data packets must be organized in specific ways according to the protocols the network supports.

### SMTP
- Simple Mail Transfer Protocol
- This protocol is important for sending and distributing outgoing emails. 
- This protocol uses the header of the mail to get the email id of the receiver and enters the mail into the queue of outgoing mail. - And as soon as it delivers the mail to the receiving email id, it removes the email from the outgoing list. The message or the electronic mail may consider the text, video, image, etc. It helps in setting up some communication server rules.
- It uses TCP
- Port # - 25

### FTP 
- File Transfer Protocol
- This protocol is used for transferring files from one system to the other. 
- This works on a client-server model. When a machine requests for file transfer from another machine, the FTP sets up a connection between the two and authenticates each other using their ID and Password. And, the desired file transfer takes place between the machines.
- It uses TCP
- Port # - 20 (Data Control) and 21 (Command Control)

### SFTP
- Secure File Transfer Protocol 
- SFTP which is also known as SSH FTP refers to File Transfer Protocol (FTP) over Secure Shell (SSH) as it encrypts both commands and data while in transmission. 
- SFTP acts as an extension to SSH and encrypts files and data then sends them over a secure shell data stream. This protocol is used to remotely connect to other systems while executing commands from the command line.
- Port # - 22

### SSH
- Secure Shell
- SSH is a protocol used for secure remote login and other secure network services. 
- It provides a secure and encrypted way to remotely access and manage servers, network devices, and other computer systems. 
- SSH uses public-key cryptography to authenticate the user and encrypt the data being transmitted, making it much more secure than traditional remote login protocols such as Telnet. 
- SSH also allows for secure file transfers using the SCP (Secure Copy) and SFTP (Secure File Transfer Protocol) protocols. 
- It uses TCP and UDP
- Port # - 22

### TELNET
- Terminal Network
- TELNET is a standard TCP/IP protocol used for virtual terminal service given by ISO. 
- This enables one local machine to connect with another. The computer which is being connected is called a remote computer and which is connecting is called the local computer. 
- TELNET operation lets us display anything being performed on the remote computer in the local computer. This operates on the client/server principle. The local computer uses the telnet client program whereas the remote computer uses the telnet server program.
- It uses TCP
- Port # - 23

### HTTP
- Hyper Text Transfer Protocol
- This protocol is used to transfer hypertexts over the internet and it is defined by the www(world wide web) for information transfer. 
- This protocol defines how the information needs to be formatted and transmitted. And, it also defines the various actions the web browsers should take in response to the calls made to access a particular web page. Whenever a user opens their web browser, the user will indirectly use HTTP as this is the protocol that is being used to share text, images, and other multimedia files on the World Wide Web. 
- It uses TCP
- Port # - 80  

### HTTPS
- HyperText Transfer Protocol Secure
- HTTPS is an extension of the Hypertext Transfer Protocol (HTTP). 
- It is used for secure communication over a computer network with the SSL/TLS protocol for encryption and authentication. 
- So, generally, a website has an HTTP protocol but if the website is such that it receives some sensitive information such as credit card details, debit card details, OTP, etc then it requires an SSL certificate installed to make the website more secure. 
- Public/private key for encryption and decryption
- It uses TCP and UDP
- Port # - 443

### POP3
- Post Office Protocol 3
- It has two Message Access Agents (MAAs) where one is client MAA (Message Access Agent) and another is server MAA(Message Access Agent) for accessing the messages from the mailbox. 
- This protocol helps us to retrieve and manage emails from the mailbox on the receiver mail server to the receiver’s computer. This is implied between the receiver and the receiver mail server.
- It uses TCP
- Port # - 110 (to retrieve e-mail from a server) and 995(secure connection)

### IMAP
- Internet Message Access Protocol
- IMAP is a protocol used for retrieving emails from a mail server. 
- It allows users to access and manage their emails on the server, rather than downloading them to a local device. This means that the user can access their emails from multiple devices and the emails will be synced across all devices. 
- IMAP is more flexible than POP3 (Post Office Protocol version 3) as it allows users to access and organize their emails on the server, and also allows multiple users to access the same mailbox.
- It uses TCP and UDP
- Port # - 143

### ICMP
- Internet Control Message Protocol
- It is a network protocol that is used to send error messages and operational information about network conditions. 
- It is an integral part of the Internet Protocol (IP) suite and is used to help diagnose and troubleshoot issues with network connectivity. 
- ICMP messages are typically generated by network devices, such as routers, in response to errors or exceptional conditions encountered in forwarding a datagram. Some examples of ICMP messages include:
    - Echo Request and Echo Reply (ping)
    - Destination Unreachable
    - Time Exceeded
    - Redirect
- ICMP can also be used by network management tools to test the reachability of a host and measure the round-trip time for packets to travel from the source to the destination and back. 
- It should be noted that ICMP is not a secure protocol, it can be used in some types of network attacks like DDoS amplification.
- Port # - ICMP has no ports and is neither TCP nor UDP

## ARP 
- Address Resolution Protocol. 
- It is a network-level protocol used to convert the logical address i.e. IP address to the device's physical address i.e. MAC address. 
- It can also be used to get the MAC address of devices when they are trying to communicate over the local network.


### TCP
- Transmission Control Protocol
- It is a connection-oriented reliable transport layer protocol
- It creates a virtual network when more than one computer is connected to the network and uses the three ways handshake model to establish the connection which makes it more reliable
- TCP is one of the main protocols of the Internet protocol suite. 
- It lies between the Application and Network Layers which are used in providing reliable delivery services. 
- It is a connection-oriented protocol for communications that helps in the exchange of messages between different devices over a network. 
- The Internet Protocol (IP), which establishes the technique for sending data packets between computers, works with TCP.

### UDP
- User Datagram Protocol
- UDP is a connectionless, unreliable transport layer protocol. 
- It is used for multicasting and broadcasting
- Unlike TCP, it does not establish a reliable connection between devices before transmitting data, and it does not guarantee that data packets will be received in the order they were sent or that they will be received at all. 
- Instead, UDP simply sends packets of data to a destination without any error checking or flow control. UDP is typically used for real-time applications such as streaming video and audio, online gaming, and VoIP (Voice over Internet Protocol) where a small amount of lost data is acceptable and low latency is important. 
- UDP is faster than TCP because it has less overhead. It doesn’t need to establish a connection, so it can send data packets immediately. 
- It also doesn’t need to wait for confirmation that the data was received before sending more, so it can transmit data at a higher rate.

## TCP vs UDP
| TCP | UDP |
|-------------------------------|-----------------------------|
| Transmission Control Protocol | User Datagram Protocol |
| Connection-oriented | Connectionless |
| Reliable, has error checking | Unreliable, no error checking |
| Uses 3 way handhshake to establish connection | No handshake |
| Slower | Faster | 
| Heavy weight packets | Lightweight packets |
| Protocols like HTTP, FTP, Telnet, SMTP, HTTPS, etc use TCP at the transport layer | Protocols like DNS, RIP, SNMP, RTP, BOOTP, TFTP, NIP, etc use UDP at the transport layer |

## HTTP Status Codes
- 1xx - Informational (request received, process in continuing)
    - 100 - Continue
    - 101 - Switching Protocol
- 2xx - Success
    - 200 - OK
- 3xx - Redirection
    - 301 - Moved Permanently
    - 302 - Found	
    - 303 - See Other
- 4xx - Client Error
    - 400 - Bad Request
    - 401 - Unauthorized
    - 403 - Forbidden
    - 404 - Page not found
- 5xx - Server Error
    - 500 - Internal Server Error
    - 502 - Bad Gateway
    - 503 - Service Unavailable


## What Happens When You Click A Link
- Browser checks cache for DNS entry to find the corresponding IP address of website. It first checks browser cache followed by OS, Router, ISP caches.
- If not found in cache, ISP’s (Internet Service Provider) DNS server initiates a DNS query to find IP address of server that hosts the domain name.
- DNS lookup using UDP to get the corresponding IP address of the URL from the DNS server to establish a new TCP connection.
- The requests are sent using small data packets that contain information content of request and IP address it is destined for.
- Browser initiates a TCP (Transfer Control Protocol) connection with the server using synchronize(SYN) and acknowledge(ACK) messages.
- Browser sends an HTTP request to the web server. GET or POST request.
- Server on the host computer handles that request and sends back a response. It assembles a response in some format like JSON, XML and HTML.
- Server sends out an HTTP response along with the status of response.
- Browser displays HTML content

## Cookies
- Cookies store information pertaining to session management, tracking and personalization. 
- The web browser stores the message/information in a text file, the message/information then sent back to the server each time the browser request a page from the server.
- The main aim of cookies is to identify users and perhaps prepare customized Web pages for them.

## Firewall
The firewall is a network security system that is used to monitor the incoming and outgoing traffic and blocks the same based on the firewall security policies. It acts as a wall between the internet (public network) and the networking devices (a private network). It is either a hardware device, software program, or a combination of both. It adds a layer of security to the network.


## Terms
- Broadcast address - An IP address with a host portion that is all ones. (last address)
- Broadcasting - message sent to all nodes
- Multicasting - message sent to subset of nodes
- Unicasting - message sent to a single destination node
- Gateways - In computer networking, a gateway is a component that is part of two networks, which use different protocols. The gateway is a protocol converter which will translate one protocol into the other. A router is a special case of a gateway.
- Host - A computer or other device on a TCP/IP network.
- Internet - The global collection of networks that are connected together and share a common range of IP addresses.
- IP - The network protocol used for sending network packets over a TCP/IP network or the Internet.
- IP Address - A unique 32-bit address for a host on a TCP/IP network or internetwork.
- ISP - Internet Service Provider, a company that provides internet access to people who pay the company or subscribe to the company
- Network - A network is a group of computers on a single physical network segment. Network can also refer to an IP network address range that is allocated by a system administrator.
- Network address - An IP address with a host portion that is all zeros.
- Node - Any communicating device in a network is called a Node. Node is the point of intersection in a network. It can send/receive data and information within a network. Examples of the node can be computers, laptops, printers, servers, modems, etc.
- Link - A link or edge refers to the connectivity between two nodes in the network. It includes the type of connectivity (wired or wireless) between the nodes and protocols used for one node to be able to communicate with the other.
- Octet - An 8-bit number, 4 of which comprise a 32-bit IP address. They have a range of 00000000-11111111 that correspond to the decimal values 0-255.
- Packet - A unit of data passed over a TCP/IP network or wide area network.
- Piggybacking - Used in bi-directional data transmission for increased efficiency, piggyback ack with to-be-sent frame
- RFC (Request for Comment) - A document used to define standards on the Internet.
- Router - A device that passes network traffic between different IP networks.
- Stop-and-wait Protocol - Send next frame only after ack of prev frame is received
- TCP/IP - Used broadly, the set of protocols, standards, and utilities commonly used on the Internet and large networks.


## Some Important Points
- ARPANET was the first network that was based on TCP/IP protocol.
- SMTP is the most commonly used internet protocol.
- The collection of the hyperlinked document on the internet known as WWW.
- MIME stands for Multipurpose Internet Mail Extension.
- Proxy server is also known as Application-level gateway.
- HDLC or High-level link control is a bit-oriented protocol that is used to transmit info from one network to another.
- Public key cryptography is a method of encrypting or signing data with two different keys and making one of the keys, the public key, available for anyone to use. The other key is known as the private key. Data encrypted with the public key can only be decrypted with the private key.
