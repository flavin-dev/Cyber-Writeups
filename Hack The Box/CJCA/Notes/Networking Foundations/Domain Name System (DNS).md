
The Domain Name System (DNS) is like the phonebook of the internet. It helps us find the right number (an IP address) for a given name (a domain such as `www.google.com`).

DNS makes our lives easier by allowing us to use human-friendly names to access online resources.

#### Domain Names vs. IP Addresses

|**Address**|**Description**|
|---|---|
|`Domain Name`|A readable address like `www.example.com` that people can easily remember.|
|`IP Address`|A numerical label (e.g., `93.184.216.34`|

#### DNS Hierarchy

DNS is organized like a tree, starting from the root and branching out into different layers.

|**Layer**|**Description**|
|---|---|
|`Root Servers`|The top of the DNS hierarchy.|
|`Top-Level Domains (TLDs)`|Such as `.com`, `.org`, `.net`, or country codes like `.uk`, `.de`.|
|`Second-Level Domains`|For example, `example` in `example.com`.|
|`Subdomains or Hostname`|For instance, `www` in `www.example.com`, or `accounts` in `accounts.google.com`.|
![[Pasted image 20260812193233.png]]


#### DNS Resolution Process (Domain Translation)

When we enter a domain name in our browser, the computer needs to find the corresponding IP address. This process is known as `DNS resolution` or `domain translation`

| **Step** | **Description**                                                                                                                                                  |
| -------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Step 1` | We type `www.example.com` into our browser.                                                                                                                      |
| `Step 2` | Our computer checks its local DNS cache (a small storage area) to see if it already knows the IP address.                                                        |
| `Step 3` | If not found locally, it queries a `recursive DNS server`. This is often provided by our Internet Service Provider or a third-party DNS service like Google DNS. |
| `Step 4` | The recursive DNS server contacts a `root server`, which points it to the appropriate `TLD name server` (such as the `.com` domains, for instance).              |
| `Step 5` | The TLD name server directs the query to the `authoritative name server` for `example.com`.                                                                      |
| `Step 6` | The authoritative name server responds with the IP address for `www.example.com`.                                                                                |
| `Step 7` | The recursive server returns this IP address to your computer, which can then connect to the website’s server directly.                                          |
`DNS Query Process`
![[Pasted image 20260812194124.png]]

