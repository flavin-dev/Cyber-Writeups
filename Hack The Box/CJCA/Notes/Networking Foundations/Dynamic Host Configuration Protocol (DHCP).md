
#### Introduction to DHCP
`DHCP` is a network management protocol used to automate the process of configuring devices on IP networks. It allows devices to automatically receive an IP address and other network configuration parameters, such as subnet mask, default gateway, and DNS servers, without manual intervention.

#### How DHCP Works
#### How DHCP Works

The DHCP process involves a series of interactions between the client (the device requesting an IP address) and the DHCP server (the service running on a network device that assigns IP addresses). This process is often referred to as `DORA`, an acronym for `Discover`, `Offer`, `Request`, and `Acknowledge`

|**Role**|**Description**|
|---|---|
|`DHCP Server`|A network device (like a router or dedicated server) that manages IP address allocation. It maintains a pool of available IP addresses and configuration parameters.|
|`DHCP Client`|Any device that connects to the network and requests network configuration parameters from the DHCP server.|

| **Step**         | **Description**                                                                                                                                                                         |
| ---------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `1. Discover`    | When a device connects to the network, it broadcasts a **DHCP Discover** message to find available DHCP servers.                                                                        |
| `2. Offer`       | DHCP servers on the network receive the discover message and respond with a **DHCP Offer** message, proposing an IP address lease to the client.                                        |
| `3. Request`     | The client receives the offer and replies with a **DHCP Request** message, indicating that it accepts the offered IP address.                                                           |
| `4. Acknowledge` | The DHCP server sends a **DHCP Acknowledge** message, confirming that the client has been assigned the IP address. The client can now use the IP address to communicate on the network. |

![[Pasted image 20260812185413.png]]


