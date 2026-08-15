
`NAT` allows multiple devices on a private network to share a single public IP address. This not only helps conserve the limited pool of public IP addresses but also adds a layer of security to the internal network.

#### Private vs. Public IP Addresses

`Public IP` addresses are globally unique identifiers assigned by Internet Service Providers (ISPs). Devices equipped with these IP addresses can be accessed from anywhere on the Internet

`Private IP` addresses are designated for use within local networks such as homes, schools, and offices. These addresses are not routable on the global internet, meaning packets sent to these addresses are not forwarded by internet backbone routers.

Defined by RFC 1918, common IPv4 private address ranges include 10.0.0.0 to 10.255.255.255, 172.16.0.0 to 172.31.255.255, and 192.168.0.0 to 192.168.255.255.

#### What is NAT?

`Network Address Translation (NAT)` is a process carried out by a router or a similar device that modifies the source or destination IP address in the headers of IP packets as they pass through. This modification is used to translate the private IP addresses of devices within a local network to a single public IP address that is assigned to the router.

![[Pasted image 20260812192817.png]]


#### Types of NAT

|**Type**|**Description**|
|---|---|
|`Static NAT`|Involves a one-to-one mapping, where each private IP address corresponds directly to a public IP address.|
|`Dynamic NAT`|Assigns a public IP from a pool of available addresses to a private IP as needed, based on network demand.|
|`Port Address Translation (PAT)`|Also known as NAT Overload, is the most common form of NAT in home networks. Multiple private IP addresses share a single public IP address, differentiating connections by using unique port numbers. This method is widely used in home and small office networks, allowing multiple devices to share a single public IP address for internet access.|

#### Benefits and Trade-Offs

|**Benefits**|
|---|
|Conserves the limited IPv4 address space.|
|Provides a basic layer of security by not exposing internal network structure directly.|
|Flexible for internal IP addressing schemes.|

| **Trade-Offs**                                                                                                         |
| ---------------------------------------------------------------------------------------------------------------------- |
| Complex services like hosting a public server behind NAT can require additional configuration (e.g., port forwarding). |
| NAT can break certain protocols that rely on end-to-end connectivity without special handling.                         |
| Adds complexity to troubleshooting connectivity issues.                                                                |
