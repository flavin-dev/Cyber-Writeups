
The goal is to uphold and maintain the `CIA triad`:

|**Principle**|**Description**|
|---|---|
|`Confidentiality`|Only authorized users can view the data.|
|`Integrity`|The data remains accurate and unaltered.|
|`Availability`|Network resources are accessible when needed.|

## Firewalls

A `Firewall` is a network security device, either hardware, software, or a combination of both, that monitors incoming and outgoing network traffic. Firewalls enforce a set of rules (known as `firewall policies` or `access control lists`) to determine whether to `allow` or `block` specific traffic.

Firewalls operate by analyzing packets of data according to predefined rules and policies, commonly focusing on factors such as IP addresses, port numbers, and protocols.

#### 1. Packet Filtering Firewall

|**Description**|
|---|
|Operates at Layer 3 (Network) and Layer 4 (Transport) of the OSI model.|
|Examines source/destination IP, source/destination port, and protocol type.|
|`Example`: A simple router ACL that only allows HTTP (port 80) and HTTPS (port 443) while blocking other ports.|

#### 2. Stateful Inspection Firewall

|**Description**|
|---|
|Tracks the state of network connections.|
|More intelligent than packet filters because they understand the entire conversation.|
|`Example`: Only allows inbound data that matches an already established outbound request.|

#### 3. Application Layer Firewall (Proxy Firewall)

|**Description**|
|---|
|Operates up to Layer 7 (Application) of the OSI model.|
|Can inspect the actual content of traffic (e.g., HTTP requests) and block malicious requests.|
|`Example`: A web proxy that filters out malicious HTTP requests containing suspicious patterns.|

#### 4. Next-Generation Firewall (NGFW)

|**Description**|
|---|
|Combines stateful inspection with advanced features like deep packet inspection, intrusion detection/prevention, and application control.|
|`Example`: A modern firewall that can block known malicious IP addresses, inspect encrypted traffic for threats, and enforce application-specific policies.|

![[Pasted image 20260813052530.png]]


## Intrusion Detection and Prevention Systems (IDS/IPS)

Intrusion Detection and Prevention Systems (IDS/IPS) are security solutions designed to monitor and respond to suspicious network or system activity. An Intrusion Detection System (IDS) observes traffic or system events to identify malicious behavior or policy violations, generating alerts but not blocking the suspicious traffic. In contrast, an Intrusion Prevention System (IPS) operates similarly to an IDS but takes an additional step by preventing or rejecting malicious traffic in real time. The key difference lies in their actions: an IDS detects and alerts, while an IPS detects and prevents.

|**Techniques**|**Description**|
|---|---|
|`Signature-based detection`|Matches traffic against a database of known exploits.|
|`Anomaly-based detection`|Detects anything unusual compared to normal activity.|

#### 1. Network-Based IDS/IPS (NIDS/NIPS)

|**Description**|
|---|
|Hardware device or software solution placed at strategic points in the network to inspect all passing traffic.|
|`Example`: A sensor connected to the core switch that monitors traffic within a data center.|

#### 2. Host-Based IDS/IPS (HIDS/HIPS)

|**Description**|
|---|
|Runs on individual hosts or devices, monitoring inbound/outbound traffic and system logs for suspicious behavior on that specific machine.|
|`Example`: An antivirus or endpoint security agent installed on a server.|
![[Pasted image 20260813052656.png]]

DMZ (Demilitarized Zone), a separate network segment within the larger network directly exposed to the internet, where they monitor traffic moving in and out of publicly accessible servers.

## Best Practices

Here are the best practices for enhancing network security, summarized in the following table:

| **Practice**                   | **Description**                                                                                                                                                                                                      |
| ------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Define Clear Policies`        | Consistent firewall rules based on the principle of `least privilege` (only allow what is necessary).                                                                                                                |
| `Regular Updates`              | Keep firewall, IDS/IPS signatures, and operating systems up to date to defend against the latest threats.                                                                                                            |
| `Monitor and Log Events`       | Regularly review firewall logs, IDS/IPS alerts, and system logs to identify suspicious patterns early.                                                                                                               |
| `Layered Security`             | Use `defense in depth` (a strategy that leverages multiple security measures to slow down an attack) with multiple layers: Firewalls, IDS/IPS, antivirus, and endpoint protection to cover different attack vectors. |
| `Periodic Penetration Testing` | Test the effectiveness of the security policies and devices by simulating real attacks.                                                                                                                              |
