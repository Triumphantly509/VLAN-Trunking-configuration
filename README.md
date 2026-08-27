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

### Why PCS in the same vlan but different switches cannot communicate?
If the link between switches is not configured as trunk, the switch will only carry one VLAN (usually VLAN 1).

### Trunking configuration
A trunk link carries multiple VLANs between switches.

### Change the link between the two switches as a trunk using Dynamic Trunking Protocol (DTP)
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/06fd4d1c-c1bf-47e2-ad2e-26848d3d2f2b" />
</div>

### DTp is on by default on the device
<div>
    <img width="600" alt="image" src="https://github.com/user-attachments/assets/59d08b77-f195-4321-be4c-e888934dc11a" />
</div>

### Dynamic Trunk Protocol
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/af43668c-3eac-402e-820c-3fcc6f245f1c" />
</div>

<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/d4b9dcf0-3c8b-4b93-9149-9179fc99d362" />
</div>

credit image: Kevin Wallace Training, LLC

### fa0/3 interface configuration on Switch 0
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/3d190301-a956-4794-b71a-d9da9ee5e7b9" />
</div>

### Allow vlan 1 and vlan 20 on switch 0
<div>
  <img width="600" height="175" alt="image" src="https://github.com/user-attachments/assets/9f558bc9-06fb-474a-9864-04c5fd5dad42" />

</div>

 ### Result 
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/5af2689f-28c3-4ce7-8013-4fba95d514f0" />
</div>


### fa0/3 interface configuration on Switch 1
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/aa41527a-902b-499f-807d-b467cc98e78a" />
</div>

### Allow vlan 1-20 on switch 1 / dynamic desirable mode
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/4845bf98-a362-4852-99ff-0b3cf66a3f9a" />
</div>

### Result
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/ef677f5f-f7cb-4be7-8fe2-b83788165e1b" />
</div>

### End results
Connectivity has been successfully established between PC1 (VLAN 20) on Switch 0 and PC3 (VLAN 20) on Switch 1.
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/c2519f19-5af8-41d5-bfc3-1b69bb72a3dc" />
</div>
