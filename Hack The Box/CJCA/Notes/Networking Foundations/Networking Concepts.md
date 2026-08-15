# Network Concepts

## OSI Model

The `Open Systems Interconnection (OSI) model` is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven abstract layers.

#### Physical Layer (Layer 1)

It is responsible for transmitting raw bitstreams over a physical medium. It deals with the physical connection between devices, including the hardware components like Ethernet cables, hubs, and repeaters.

#### Data Link Layer (Layer 2)

It ensures that data frames are transmitted with proper synchronization, error detection, and correction. Devices such as switches and bridges operate at this layer, using [MAC (Media Access Control)](https://en.wikipedia.org/wiki/MAC_address) addresses to identify network devices.

#### Network Layer (Layer 3)

It is responsible for logical addressing and path determination, ensuring that data reaches the correct destination across multiple networks. Routers operate at this layer, using [IP (Internet Protocol) addresses](https://usa.kaspersky.com/resource-center/definitions/what-is-an-ip-address?srsltid=AfmBOoq0TltVlJi8PKDn6j4yNB0V5Av5Y4srTxb32Bbbg4TcAfZ5FG8H) to identify devices and determine the most efficient path for data transmission.

#### Transport Layer (Layer 4)

It is responsible for the reliable (or unreliable) delivery of data, segmentation, reassembly of messages, flow control, and error checking. Protocols like `TCP (Transmission Control Protocol)` and `UDP (User Datagram Protocol)` function at this layer.

#### Session Layer (Layer 5)

It establishes, maintains, and terminates connections, allowing devices to hold ongoing communications known as sessions. This layer is essential for session checkpointing and recovery, ensuring that data transfer can resume seamlessly after interruptions. Protocols and `APIs (Application Programming Interfaces)` operating at this layer coordinate communication between systems and applications.

#### Presentation Layer (Layer 6)

It handles data representation, ensuring that information sent by the application layer of one system is readable by the application layer of another. This includes data encryption and decryption, data compression, and converting data formats

#### Application Layer (Layer 7)

It enables resource sharing, remote file access, and other network services. Common protocols operating at this layer include `HTTP (Hypertext Transfer Protocol)` for web browsing, `FTP (File Transfer Protocol)` for file transfers, `SMTP (Simple Mail Transfer Protocol)` for email transmission, and `DNS (Domain Name System)` for resolving domain names to IP addresses. This layer serves as the interface between the network and the application software.


![[Pasted image 20260810195618.png]]


#### Example of Sending a File Across Network Layers

When sending a file over a network, several steps occur across different layers of the network model. The process begins at the `Application Layer`, which initiates the file transfer request. Following this, the `Presentation Layer` encrypts the file to ensure its security during transmission. The `Session Layer` then establishes a communication session with the receiving device. At the `Transport Layer`, the file is broken down into segments to ensure error-free transmission. The `Network Layer` takes over to determine the best route for transferring the data across the network. Next, the `Data Link Layer` encapsulates the data into frames, preparing it for node-to-node delivery. Finally, the `Physical Layer` handles the actual transmission of bits over the physical medium, completing the process.




## TCP/IP Model

The `Transmission Control Protocol/Internet Protocol (TCP/IP) model` is a condensed version of the `OSI` model, tailored for practical implementation on the internet and other networks.

#### Link Layer

The Link Layer corresponds to the Physical and Data Link Layers of the OSI model, covering everything from the physical connection to data framing.

#### Internet Layer

Protocols like IP (Internet Protocol) and ICMP (Internet Control Message Protocol) operate at this layer
This layer corresponds to the Network Layer in the OSI model.

#### Transport Layer

This includes the use of TCP (Transmission Control Protocol) for reliable communication and UDP (User Datagram Protocol)

corresponds to the Transport Layer of the OSI model.

#### Application Layer

Protocols such as HTTP (Hypertext Transfer Protocol), FTP (File Transfer Protocol), and SMTP (Simple Mail Transfer Protocol) enable functionalities like web browsing, file transfers, and email services. This layer corresponds to the top three layers of the OSI model (Session, Presentation, and Application), providing interfaces and protocols necessary for data exchange between systems.

![[Pasted image 20260810200830.png]]


## Protocols

`Protocols` are standardized rules that determine the formatting and processing of data to facilitate communication between devices in a network.

#### Common Network Protocols

Network protocols are essential for defining how data is exchanged across networks. Each protocol operates at a specific layer of the OSI model, ensuring structured and efficient data handling.

| **Protocol**                           | **Description**                                                                                                                                                                                                                      |
| -------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `HTTP (Hypertext Transfer Protocol)`   | Primarily used for **transferring web pages**. It operates at the **Application Layer**, allowing browsers and servers to communicate in the delivery of web content.                                                                |
| `FTP (File Transfer Protocol)`         | Facilitates the transfer of files between systems, also functioning at the **Application Layer**. It provides a way for users to **upload or download files to and from servers**.                                                   |
| `SMTP (Simple Mail Transfer Protocol)` | Handles the transmission of email. Operating at the **Application Layer**, it is responsible for sending messages from one server to another, **ensuring they reach their intended recipients**.                                     |
| `TCP (Transmission Control Protocol)`  | Ensures reliable data transmission through error checking and recovery, operating at the **Transport Layer**. It establishes a connection between sender and receiver to **guarantee the delivery of data in the correct order**.    |
| `UDP (User Datagram Protocol)`         | Allows for fast, connectionless communication, which operates without error recovery. This makes it ideal for applications that require speed over reliability, such as streaming services. UDP operates at the **Transport Layer**. |
| `IP (Internet Protocol)`               | Crucial for routing packets across network boundaries, functioning at the **Internet Layer**. It handles the **addressing and routing of packets to ensure they travel from the source to the destination across diverse networks**. |


## Transmission

`Transmission` in networking refers to the process of sending data signals over a medium from one device to another.

#### Transmission Types

Transmission in networking can be categorized into two main types: `analog` and `digital` 

Analog transmission uses continuous signals to represent information
eg.radio

digital transmission employs discrete signals (bits) to encode data, which is typical in modern communication technologies like computer networks

#### Transmission Modes

`Simplex` mode allows one-way communication only, such as from a keyboard to a computer, where signals travel in a single direction.
`Half-duplex` mode permits two-way communication but not simultaneously; examples include walkie-talkies
`Full-duplex` mode, used in telephone calls, supports two-way communication simultaneously

#### Transmission Media

The physical means by which data is transmitted in a network is known as transmission media, which can be wired or wireless

`twisted pair` cables, commonly used in Ethernet networks and local area network (LAN) connections; 
`coaxial` cables, used for cable TV and early Ethernet; 
`fiber optic` cables, which transmit data as light pulses and are essential for high-speed internet backbones. 
Wireless media, on the other hand, encompasses `radio waves` for Wi-Fi and cellular networks, 
`microwaves` for satellite communications, and `infrared` technology used for short-range communications like remote controls.

