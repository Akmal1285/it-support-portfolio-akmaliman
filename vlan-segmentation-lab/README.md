Project: Network Segmentation via VLANs
📌 Project Overview
This project demonstrates the implementation of Virtual Local Area Networks (VLANs) on a Cisco Layer 2 Switch. The objective was to logically isolate two different departments (Sales and HR) using a single physical switch to enhance network security and reduce broadcast traffic.

🛠️ Technical Stack
Simulation Tool: Cisco Packet Tracer

Hardware: 1x Cisco Catalyst 2960 Switch

End Devices: 2x Generic PCs (Sales-PC and HR-PC)

Protocol: IEEE 802.1Q (VLAN Tagging)

🚀 Step-by-Step Implementation
1. Physical Connectivity
I started by connecting two PCs to the switch using Copper Straight-Through cables:

Sales-PC connected to port FastEthernet 0/1

HR-PC connected to port FastEthernet 0/2

2. Initial Connectivity (Baseline)
Before applying any configuration, I assigned both PCs to the 192.168.1.0/24 subnet:

Sales-PC: 192.168.1.1

HR-PC: 192.168.1.2

Test: A ping was successful, proving that by default, all ports on a switch belong to VLAN 1 (the management VLAN).

3. Creating the Logical Segments
Using the Cisco IOS CLI, I created two distinct VLANs to act as "security containers" for the departments.

Bash
Switch> enable
Switch# configure terminal
Switch(config)# vlan 10
Switch(config-vlan)# name Sales
Switch(config-vlan)# exit
Switch(config)# vlan 20
Switch(config-vlan)# name HR
4. Assigning Ports to VLANs
I then moved the physical ports into their respective virtual networks. This "locks" the port so it only talks to other members of the same VLAN.

Bash
! Assigning Port 1 to Sales
Switch(config)# interface fa0/1
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 10

! Assigning Port 2 to HR
Switch(config)# interface fa0/2
Switch(config-if)# switchport mode access
Switch(config-if)# switchport access vlan 20
✅ Verification & Results
VLAN Database Check
To verify the configuration, I used the show vlan brief command.

Result: Port Fa0/1 is active in VLAN 10 (Sales).

Result: Port Fa0/2 is active in VLAN 20 (HR).

Connectivity Isolation Test
I attempted to ping the HR-PC from the Sales-PC.

Result: Request Timed Out. * Conclusion: Even though the PCs are physically connected to the same switch and have valid IP addresses on the same subnet, the switch is now successfully blocking traffic between them at Layer 2.

💡 Key Lessons Learned
Logical vs. Physical: Network security isn't just about physical cables; it's about logical software control.

Security: By isolating departments, we prevent unauthorized access to sensitive data and stop the spread of potential network threats (like malware) from one department to another.