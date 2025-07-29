# network-lab-01
Basic network configuration using VLANs and IP addressing in Cisco Packet Tracer
# 🖧 Network Lab 01 – Basic VLAN, IP Configuration & Ping Test

This lab demonstrates the creation of a basic LAN environment using Cisco Packet Tracer. It includes:
- Switch and router configuration
- Static IP assignment
- VLAN setup
- Connectivity testing using the ping command

---

## 🛠️ Lab Objectives

- Connect three PCs to a switch and a router
- Assign static IP addresses to all PCs
- Create VLANs on the switch
- Configure the router interface
- Test end-to-end connectivity using ping

---

## 🧪 Screenshots & Configurations

| Step | Description | Filename |
|------|-------------|----------|
| 1 | Logical topology view of the network (PCs, Switch, Router) | `01_LogicalTopology.png` |
| 2 | VLAN 20 created and named “sales” | `02_VLAN_Config_Switch1.png` |
| 3 | VLAN 10 created and named “admin” | `03_VLAN_Config_Switch1_Admin.png` |
| 4 | Interface FastEthernet0/0 configured with IP `192.168.1.1` on Router | `04_Router_Interface_Config.png` |
| 5 | PC0 assigned IP `192.168.1.10`, no gateway | `05_PC0_IP_Config.png` |
| 6 | PC1 assigned IP `192.168.1.11`, no gateway | `06_PC1_IP_Config.png` |
| 7 | PC2 assigned IP `192.168.1.12`, gateway `192.168.1.1` | `07_PC2_IP_Config_With_Gateway.png` |
| 8 | PC2 ping test to 192.168.1.10 and .11 – Success | `08_PC2_Ping_Test.png` |
| 9 | PC0 ping test to PC1 and router – Success | `09_PC0_Ping_Test.png` |
| 10 | Command line interface showing successful ping replies | `10_CLI_Ping_Stats.png` |
| 11 | Final view of the fully connected network | `11_Final_Topology.png` |

---

## 💡 Commands Used

enable
configure terminal
vlan 10
name admin
exit
vlan 20
name sales
exit

interface FastEthernet0/0
ip address 192.168.1.1 255.255.255.0
no shutdown
exit
show Vlan brief
