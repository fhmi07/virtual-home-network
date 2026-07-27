# IP Addressing Plan

## Network Information

Network:
192.168.10.0/24

Subnet Mask:
255.255.255.0


## Static Devices

| Device | IP Address |
|---|---|
| Home-Router | 192.168.10.1 |
| Home-Server | 192.168.10.10 |
| Network-Printer | 192.168.10.20 |


## DHCP Range

192.168.10.100 - 192.168.10.200


## Future VLAN Expansion

| VLAN | Purpose | Network |
|---|---|---|
| VLAN 10 | Personal Devices | 192.168.10.0/24 |
| VLAN 20 | IoT Devices | 192.168.20.0/24 |
| VLAN 30 | Guest Network | 192.168.30.0/24 |
| VLAN 40 | Servers | 192.168.40.0/24 |