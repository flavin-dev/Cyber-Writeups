
#### 1. Accessing the Internet

|**Steps**|
|---|
|The laptop first identifies the correct wireless network/SSID|
|If the network uses WPA2/WPA3, the user must provide the correct password or credentials to authenticate.|
|Finally, the connection is established, and the DHCP protocol takes over the IP configuration.|

#### 2. Checking Local Network Configuration (DHCP)

|**Steps**|**Description**|
|---|---|
|`IP Address Assignment`|If the laptop does not already have an IP, it requests one from the home router's `DHCP` server. This IP address is only valid within the local network.|
|`DHCP Acknowledgement`|The DHCP server assigns a private IP address (for example, _192.168.1.10_) to the laptop, along with other configuration details such as subnet mask, default gateway, and DNS server.|

#### 3. DNS Resolution

|**Steps**|**Description**|
|---|---|
|`DNS Query`|The laptop sends a DNS query to the DNS server, which is typically an external DNS server provided by the ISP or a third-party service like Google DNS.|
|`DNS Response`|The DNS server looks up the domain `www.example.com` and returns its IP address (e.g., 93.184.216.34).|
#### 4. Data Encapsulation and Local Network Transmission

|**Steps**|**Description**|
|---|---|
|`Application Layer`|The browser creates an HTTP (or HTTPS) request for the webpage.|
|`Transport Layer`|The request is wrapped in a TCP segment (or UDP, but for web traffic it's typically TCP). This segment includes source and destination ports (HTTP default port 80, HTTPS default port 443).|
|`Internet Layer`|The TCP segment is placed into an IP packet. The source IP is the laptop's private IP (e.g., 192.168.1.10), and the destination IP is the remote server’s IP (93.184.216.34).|
|`Link Layer`|The IP packet is finally placed into an Ethernet frame (if we're on Ethernet) or Wi-Fi frame. Here, the MAC (Media Access Control) addresses are included (source MAC is the laptop's network interface, and destination MAC is the router's interface).|

#### 5. Network Address Translation (NAT)

Once the router receives the frame, it processes the IP packet. At this point, the router replaces the private IP (192.168.1.10) with its public IP address (e.g., 203.0.113.45) in the packet header. This process is known as `Network Address Translation (NAT)`.

#### 6. Server Receives the Request and Responds

Upon reaching the destination network, the server's firewall, if there is one, checks if the incoming traffic on port 80 (HTTP) or 443 (HTTPS) is allowed. If it passes firewall rules, it goes to the server hosting `www.example.com`. Next, the web server software (e.g., Apache, Nginx, IIS) receives and processes the request, prepares the webpage (HTML, CSS, images, etc.), and sends it back as a response.

#### 7. Decapsulation and Display

Finally, our laptop receives the response and strips away the Ethernet/Wi-Fi frame, the IP header, and the TCP header, until the application layer data is extracted. The laptop's browser reads the HTML/CSS/JavaScript, and ultimately displays the webpage.

#### Data Flow Diagram

![[Pasted image 20260813053835.png]]

