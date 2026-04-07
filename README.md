# VLAN-Trunking-configuration

## Objective


## Skills learned

## Tools used

## Commands Practiced

## Lab Topology
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/1363d58a-7979-4e48-bf12-adb0370ea314" />
</div>

### The issue
Host in VLAN 1 cannot communicate with the ones in VLan 20

<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/5f53cb09-6182-4d2a-afb1-a704926f8218" />
</div>

### Why some PCS cannot communicate?
If the link between switches is not configured as trunk, the switch will only carry one VLAN (usually VLAN1).

### Trunking configuration
A trunk link carries multiple VLANs between switches.

### Changing the link between the two switches as a trunk using Dynamic Trunking Protocol (DTP)
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

### Turning fa0/3 into a trunk

### fa0/3 interface configuration
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/3d190301-a956-4794-b71a-d9da9ee5e7b9" />
</div>

### Allow vlan 1-20 on switch 1 / dynamic desirable mode
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/185b4b88-bcd1-4993-9bdd-69c2f164ce78" />
</div>

### Allow vlan 1-20 on switch 1 / dynamic auto mode
<div>
  <img width="600" alt="image" src="https://github.com/user-attachments/assets/29733871-3ac1-4a55-b719-530b0381a2be" />
</div>
