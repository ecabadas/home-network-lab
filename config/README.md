# Configs

Real config files stay off this repo. They have my actual network details in them, and those don't go online.

How the network is put together:

- **Gateway:** UniFi Cloud Gateway Max, managed through the UniFi controller. WAN on auto-negotiation with hardware acceleration on (the full story is in [troubleshooting/wan-throughput-degradation.md](../troubleshooting/wan-throughput-degradation.md)).
- **Segmentation:** Separate VLANs for my main network, IoT devices, and guests. The trust model is simple: IoT and guest segments can reach the internet but can't initiate connections into the main network.
- **Wireless:** Each SSID drops clients into its own VLAN, so a guest phone never touches the main network.
- **DNS/DHCP:** Handled by the gateway, one scope per VLAN.
- **Power:** Modem, gateway, and switch all sit on a UPS (APC Back-UPS), so short outages don't take the network down.
- **Backups:** I take a console backup before every firmware update or maintenance window. No exceptions.

VLAN IDs, subnets, SSID names, and anything credential-shaped stay private. If a write-up ever needs a config snippet, it'll go here with the real values swapped for placeholders.
