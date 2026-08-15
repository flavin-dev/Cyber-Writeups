
|**Component**|**Description**|
|---|---|
|`End Devices`|Computers, Smartphones, Tablets, IoT / Smart Devices|
|`Intermediary Devices`|Switches, Routers, Modems, Access Points|
|`Network Media and Software Components`|Cables, Protocols, Management and Firewalls Software|
|`Servers`|Web Servers, File Servers, Mail Servers, Database Servers|

## End Devices

An `end device`, also known as a `host`, is any device that ultimately ends up sending or receiving data within a network

## Intermediary Devices

An `intermediary device` has the unique role of facilitating the flow of data between `end devices`, either within a local area network, or between different networks. These devices include routers, switches, modems

#### Network Interface Cards (NICs)

A `Network Interface Card (NIC)` is a hardware component installed in a computer, or other device, that enables connection to a network. It provides the physical interface between the device and the network media, handling the sending and receiving of data over the network. Each NIC has a unique Media Access Control (MAC) address, which is essential for devices to identify each other, and facilitate communication at the data link layer.

#### Routers

A `router` is an intermediary device that plays a hugely important role: the forwarding of data packets between networks, and ultimately directing internet traffic. Operating at the network layer (Layer 3) of the OSI model

They use routing tables and routing protocols such as `Open Shortest Path First (OSPF)` or `Border Gateway Protocol (BGP)` to find the most efficient path for data to travel across interconnected networks, including the internet.

#### Switches

The `switch` , its primary job being to connect multiple devices within the same network, typically a Local Area Network (LAN).

For instance, in a corporate office, switches connect employees' computers, allowing for quick file sharing and access to shared resources like printers and servers.

#### Hubs

A `hub` is a basic (and now antiquated) networking device. It connects multiple devices in a network segment and broadcasts incoming data to all connected ports, regardless of the destination.
Operating at the physical layer (Layer 1) of the OSI model
do not manage traffic intelligently.
hubs less suitable for modern networks

## Network Media and Software Components

`Network Media and Software Components` are vital elements that enable seamless communication and operation within a network. 

`Network media`, such as cables and wireless signals, provide the physical pathways that connect devices and allow data to be transmitted between them.

`software components` like network protocols and management software define the rules and procedures for data transmission, ensuring that information is correctly formatted, addressed, transmitted, routed, and received.

#### Cabling and Connectors

`Cabling and connectors` are the physical materials used to link devices within a network, forming the pathways through which data is transmitted.

For example, in an office setting, Ethernet cables with RJ-45 connectors might connect desktop computers to network switches, enabling high-speed data transfer across the local area network.

#### Network Protocols

`Network protocols` are the set of rules and conventions that control how data is formatted, transmitted, received, and interpreted across a network.

Protocols encompass a wide range of aspects such as:

- `Data Segmentation`
- `Addressing`
- `Routing`
- `Error Checking`
- `Synchronization`

Common network protocols include:

- `TCP/IP`: ubiquitous across all internet communications
- `HTTP/HTTPS`: The standard for Web traffic
- `FTP`: File transfers
- `SMTP`: Email transmissions


#### Network Management Software

`Network management software` consists of tools and applications used to monitor, control, and maintain network components and operations.

These software solutions provide functionalities for:

- `performance monitoring`
- `configuration management`
- `fault analysis`
- `security management`

#### Software Firewalls

A `software firewall` is a security application installed on individual computers or devices that monitors and controls incoming and outgoing network traffic based on predetermined security rules.

## Servers

A `server` is a powerful computer designed to provide services to other computers, known as clients, over a network. Servers are the backbone behind websites, email, files, and applications.


## Conclusion

As we have seen, the technology stack needed for world-wide computer networking requires multiple components. End devices are the users' primary interface with the network, intermediary devices manage data traffic and connectivity, and servers provide resources and services. Together, they enable the seamless flow of information that powers modern communication.


