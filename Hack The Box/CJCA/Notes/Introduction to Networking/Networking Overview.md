

There is a wide array of `topologies` (mesh/tree/star), `mediums` (ethernet/fiber/coax/wireless), and `protocols` (TCP/UDP/IPX) that can be used to facilitate the network.

Most networks use a `/24` subnet
The /24 network allows computers to talk to each other as long as the first three octets of an IP Address are the same (ex: 192.168.1.xxx).

Setting the subnet mask to `/25` divides this range in half, and the computer will be able to talk to only the computers on "its half."

- Server Gateway: 10.20.0.1/25
- Domain Controller: 10.20.0.10/25
- Client Gateway: 10.20.0.129/25
- Client Workstation: 10.20.0.200/25
- Pentester IP: 10.20.0.252/24 (Set Gateway to 10.20.0.1)

high-level diagram of how a Work From Home setup may work.

![[Pasted image 20260816191455.png]]

---

The entire internet is based on many subdivided networks, as shown in the example and marked as "`Home Network`" and "`Company Network`." 

We can imagine `networking` as the delivery of mail or packages sent by one computer and received by the other.

The website address or `Uniform Resource Locator` (`URL`) which we enter into our browser is also known as `Fully Qualified Domain Name` (`FQDN`).

The difference between `URL`s and `FQDN`s is that:

- an `FQDN` (`www.hackthebox.eu`) only specifies the address of the "building" and
- an `URL` (`https://www.hackthebox.eu/example?floor=2&office=dev&employee=17`) also specifies the "`floor`," "`office`," "`mailbox`" and the corresponding "`employee`" for whom the package is intended.

