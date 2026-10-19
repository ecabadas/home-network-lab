# Network Topology & Inventory

## Topology

<img width="714" height="966" alt="HomeNetworkTopo drawio" src="https://github.com/user-attachments/assets/cf3576a1-4680-4d89-a5ea-e5894c2d371b" />


         
Physical path: ISP coax → modem → gateway WAN (2.5 GbE) → gateway LAN → PoE switch → patch panel → room drops; access point powered via PoE.

## Inventory

| Device | Model | Role |
|---|---|---|
| Modem | Arris Surfboard S33 | DOCSIS 3.1 modem, 2.5 GbE uplink |
| Gateway | Ubiquiti Cloud Gateway Max (base, no storage) | Router, firewall, UniFi controller host |
| Switch | USW-Flex 2.5G-8-PoE | LAN distribution, AP power |
| Access point | UniFi U7 Lite (AP) | Wireless coverage |
| Patch panel | 12-port Cat6 | Terminates in-wall drops |
| UPS | APC Back-UPS (600VA) | Battery backup for modem, gateway, and switch |

## Segmentation

- Separate SSIDs on separate VLANs for main, IoT, and guest traffic (VLAN IDs and subnets obscured)
- Wired drops home-run to the patch panel

## Notes

- IP addresses, MAC addresses, and wireless network names are obscured in this repo 
