
Each network is structured differently and can be set up individually
`types` and `topologies` have been developed that can be used to categorize these networks.

#### Common Terminology

|**Network Type**|**Definition**|
|---|---|
|Wide Area Network (WAN)|Internet|
|Local Area Network (LAN)|Internal Networks (Ex: Home or Office)|
|Wireless Local Area Network (WLAN)|Internal Networks accessible over Wi-Fi|
|Virtual Private Network (VPN)|Connects multiple network sites to one `LAN`|

## WAN

The WAN (Wide Area Network) is commonly referred to as `The Internet`.

## LAN / WLAN

LANs (Local Area Network) and WLANs (Wireless Local Area Network) will typically assign IP Addresses designated for local use (RFC 1918, 10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16).

## VPN

There are three main types `Virtual Private Networks` (`VPN`), but all three have the same goal of making the user feel as if they were plugged into a different network.

#### Site-To-Site VPN

Both the client and server are Network Devices, typically either `Routers` or `Firewalls`, and share entire network ranges. This is most commonly used to join company networks together over the Internet, allowing multiple locations to communicate over the Internet as if they were local.

#### Remote Access VPN

This involves the client's computer creating a virtual interface that behaves as if it is on a client's network.
If the VPN only creates routes for specific networks (ex: 10.10.10.0/24), this is called a `Split-Tunnel VPN`, meaning the Internet connection is not going out of the VPN.
for a company, `split-tunnel` VPN's are typically not ideal because if the machine is infected with malware, network-based detection methods will most likely not work as that traffic goes out the Internet.

#### SSL VPN

This is essentially a VPN that is done within our web browser and is becoming increasingly common as web browsers are becoming capable of doing anything. Typically these will stream applications or entire desktop sessions to your web browser.


## Book Terms

|Network Type|Definition|
|---|---|
|Global Area Network (GAN)|Global network (the Internet)|
|Metropolitan Area Network (MAN)|Regional network (multiple LANs)|
|Wireless Personal Area Network (WPAN)|Personal network (Bluetooth)|

#### GAN

A worldwide network such as the `Internet` is known as a `Global Area Network` (`GAN`).
`GAN`s use the glass fibers infrastructure of wide-area networks and interconnect them by international undersea cables or satellite transmission.

#### MAN

`Metropolitan Area Network` (`MAN`) is a broadband telecommunications network that connects several `LAN`s in geographical proximity. As a rule, these are individual branches of a company connected to a `MAN` via leased lines.

Cities wired as `Metropolitan Area Networks` can be integrated supra-regionally in `Wide Area Networks` (`WAN`) and internationally in `Global Area Networks` (`GAN`).

#### PAN / WPAN

Modern end devices such as smartphones, tablets, laptops, or desktop computers can be connected ad hoc to form a network to enable data exchange. This can be done by cable in the form of a `Personal Area Network` (`PAN`).



