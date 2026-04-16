**Cisco Networking Lab Project**

**Project Overview**

This project demonstrates a basic enterprise-style network using Cisco devices. It includes network design, IP addressing, device configuration, troubleshooting, and packet analysis using simulation tools.

**Step-by-Step Implementation Guide**

Step 1: Install Required Tools
Download and install Cisco Packet Tracer (from Cisco Networking Academy)
Install Wireshark for packet analysis

**Step 2: Create Network Topology**

**Open Cisco Packet Tracer and build the following setup:**

1 Router (R1)
1 Switch (S1)
2 PCs (PC1, PC2)
Physical Connections:
PC1 → Switch (Fa0/1)
PC2 → Switch (Fa0/2)
Switch → Router (Gig0/0)

**Step 3: IP Addressing Scheme**

**Assign the following IP addresses:**

Device	IP Address	Subnet Mask
PC1	192.168.1.10	255.255.255.0
PC2	192.168.1.11	255.255.255.0
Router (G0/0)	192.168.1.1	255.255.255.0

Default Gateway for PCs: 192.168.1.1

**Step 4: Configure Router (R1)**

Enter CLI and apply configuration:

enable
configure terminal


interface gig0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit


write memory

**Step 5: Configure Switch (S1)**


Basic switch configuration:

enable
configure terminal


interface range fa0/1 - 2
switchport mode access
no shutdown
exit


write memory

**Step 6: Configure PCs**

On each PC:

Go to Desktop → IP Configuration
Enter IP address, subnet mask, and default gateway

**Step 7: Test Connectivity**

Run the following tests:

Ping PC1 → PC2
Ping PC1 → Router (192.168.1.1)
Ping PC2 → Router

Expected result: All devices should reply successfully.

**Step 8: Troubleshooting Scenarios**

Issue 1: No connectivity between devices
Cause: Incorrect IP configuration
Fix: Verify subnet mask and IP address
Issue 2: Interface down on router
Cause: Interface shutdown
Fix: Use no shutdown
Issue 3: Ping fails
Cause: Wrong default gateway
Fix: Set gateway to router IP
Step 9: Packet Analysis (Wireshark)
Capture ICMP packets during ping
Observe request and reply flow
Analyze TCP handshake if applicable

**Tools Used**

Cisco Packet Tracer
Wireshark

**Skills Demonstrated**

Network design and topology creation
IP addressing and subnetting
Cisco router and switch configuration
Basic network troubleshooting
Packet analysis using Wireshark

**How to Use This Project**

Open Cisco Packet Tracer
Build the topology as described
Apply configurations step by step
Test connectivity using ping
Analyze packets using Wireshark

**Outcome**

This project demonstrates foundational networking skills required for entry-level Network Engineer and IT Support roles.

👤 Author

Archana Puppala Network Engineer | Cisco Networking | IT Infrastructure Enthusiast
