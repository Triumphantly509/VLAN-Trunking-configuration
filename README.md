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
