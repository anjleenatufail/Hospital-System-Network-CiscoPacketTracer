# Hospital-System-Network-Design

**Objective**

The motivation of this project is to design a Hospital System Network and meet all the requirements of infrastructure. All the departments will be on a separate network segment and Access Control Lists and Virtual Private Network (VPN) is also implemented to enable secure communication considering security and network performance factors.

**Details of design**

The Hospital System has two locations and 6 departments within both locations. The main 
headquarter includes Medical Lead Operation & Consultancy Services (MLOCS), Medical Emergency and 
Reporting (MER), Medical Records Management (MRM), Information Technology (IT), and Customer 
Service (CS). The branch headquarter includes Nurses & Surgery Operations (NSO), Hospital Labs (HL), Human 
resource (HR), Marketing (MK), and Finance (FIN). One department of Guest Waiting Area (GWA) in both locations.
Each department is required to have a wireless network for the users.
Every department in HQ is estimated to have around 60 users while in Branch to have 30 users.
Each department should be in a different VLAN and a different subnetwork.
Provided a base network of 192.168.100.0, and carry out subnetting to allocate the correct number of IP addresses to each department.
The company network is connected to the static, public IP addresses (Internet Protocol) 195.136.17.0/30, 195.136.17.4/30, 195.136.17.8/30, and 195.136.17.12/30 connected to the two Internet providers. Use OSPF as the routing protocol to advertise routes both on the routers and multilayer switches.
Configure default static routing to enable routers and multilayer switches to forward any traffic that does not match routing table entries. Use next-hop IP addresses.
Configure SSH in all the routers and layer three switches for remote login.
Configure port-security for the server site department switch to allow only one device to connect to a switch port, use sticky method to obtain mac-address and violation mode shutdown.
Configure the extended ACL rule together with site-to-site VPN (IPSec VPN) to create a tunnel and encrypt communication between HQ and the Branch network.
Configure PAT to use the respective outbound router interface IPv4 address, and implement the necessary ACL rule.

**Network Technology implementation sequence**

1. Hierarchical Network Design
2. Connecting Networking devices with Correct cabling
3. Configuring Basic device settings such as hostnames, console password, enable password, banner messages, and disable IP domain lookup and SSH for secure Remote access on Switches and Routers
4. Creating VLANs and assigning ports VLAN numbers and Configuring Inter-VLAN Routing on the Multilayer switches (Switch Virtual Interface) on L2, L3
5. Switchport security to server-side site
6. Subnetting and IP Addressing
7. Configuring ISP routers
8. Configuring OSPF as the routing protocol and default static routing used next-hop IP addresses
9. Configuring Server side statically IP address according to VLAN address, then making DHCP Server device to provide dynamic IP allocation
10. Configuring Inter-VLAN routing on L3 switches
11. Configuring host devices and WLAN or wireless network (Cisco Access Point)
12. Configuring NAT Overload (Port Address Translation PAT)
13. Configuring standard and extended Access Control Lists ACL
14. Configuring Site-to-Site IPsec VPN
