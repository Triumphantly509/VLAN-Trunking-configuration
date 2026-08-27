# VLAN-Trunking-configuration

## Objective
To configure VLANs on multiple switches, assign interfaces to the appropriate VLANs, and verify end-to-end connectivity across switches using trunk links.

## Skills learned
- Configuring and managing VLANs on Cisco switches
- Assigning access ports to specific VLANs
- Configuring and verifying trunk links between switches (802.1Q)
- Understanding VLAN segmentation and broadcast domains
- Verifying network configurations using CLI commands
- Troubleshooting VLAN and trunking issues 
- Validating end-to-end connectivity between devices within the same VLAN across multiple switches
  
## Tools used
- Cisco Packet Tracer
- Cisco Switch CLI (IOS)
- Network simulation environment

## Commands Practiced
- enable
- configure terminal
- vlan 1, vlan 20
- name <vlan-name>
- interface fa0/x
- switchport mode access
- switchport access vlan <vlan-id>
- interface fa0/1
- switchport mode trunk
- switchport trunk allowed vlan 1,20
- show vlan brief
- show interfaces trunk
- show interfaces <interface> switchport
- copy running-config startup-config

## Lab Topology
<div>
  <img width="1001" height="452" alt="image" src="https://github.com/user-attachments/assets/11914602-caa7-4496-b0f3-e17da8cda95a" />
</div>

### Display vlan configuration on switch3

## Show Vlan brief result

<div>
  <img width="626" height="239" alt="image" src="https://github.com/user-attachments/assets/66730746-073f-4989-b0a2-73a7b603c11c" />
</div>

## Show int fa0/2 switchport result

<div>
  <img width="577" height="405" alt="image" src="https://github.com/user-attachments/assets/c998feb9-3111-4d71-b6b1-430b4e53e73e" />
</div>

## show interface Trunk result
<div>
  <img width="631" height="195" alt="image" src="https://github.com/user-attachments/assets/d6797b51-8299-42bb-a141-5e02cd680fe5" />
</div>

## Display vlan configuration on switch4

### Show Vlan brief result

<div>
  <img width="678" height="240" alt="image" src="https://github.com/user-attachments/assets/f415ee96-7d3c-4c47-98d0-20056b3e53d7" />
</div>

## Show int fa0/2 switchport result

<div>
  <img width="877" height="368" alt="image" src="https://github.com/user-attachments/assets/2c23bdc9-8bee-4071-8706-ff65a020edeb" />
</div>

## show interface Trunk result
<div>
  <img width="652" height="195" alt="image" src="https://github.com/user-attachments/assets/6a4a416c-4176-4735-aa3b-de7f132b93b1" />
</div>

### VLANS are Logical

PC6 and PC10 are connected to different physical switches.

PC6 is connected to switch3 vs PC10 is connected to switch4

Both are in VLAN 10, VLAN10 exist in both switches.

The same thing happens with VLAN 20 as well, VLAN 20 exists on switch3 & 4

### Trunking rules

<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/d4b9dcf0-3c8b-4b93-9149-9179fc99d362" />
</div>

credit image: Kevin Wallace Training, LLC

### The trunk link

The Dashed link between the switches is the trunk link.

A trunk is used to carry traffic belonging to multiple VLANs between switches.

In this topology, the trunk carries VLAN 10 & VLAN 20.

Without the trunk, VLAN 10 on Switch3 would be isolated from VLAN 10 on Switch4.

Likewise, VLAN 20 on Switch3 would be isolated from VLAN 20 on Switch4.



