# DHCP Configuration Lab

## Objective

Configure Dynamic Host Configuration Protocol (DHCP) so client devices can obtain their network settings automatically, then verify connectivity.

## Project file

Upload the Packet Tracer project file into this folder as:

`DHCP-Lab.pkt`

## Lab documentation

Record the values shown in the actual topology and device configuration:

- DHCP server or router providing the leases
- DHCP pool name
- Network address and subnet mask
- Default gateway
- DNS server, if configured
- Address range and excluded addresses
- Client lease details

## Useful verification commands

On a Cisco IOS DHCP server/router:

```text
show ip dhcp pool
show ip dhcp binding
show ip dhcp server statistics
show running-config
```

On client PCs in Packet Tracer, use the Desktop > IP Configuration panel and verify that the assigned IP address, subnet mask, default gateway, and DNS settings match the intended network.

Test connectivity with:

```text
ipconfig
ping <default-gateway>
ping <destination-ip>
```

## Evidence

Add screenshots of the topology, DHCP configuration, client lease details, and successful connectivity tests.

> Do not publish passwords, private keys, or other credentials in screenshots or configuration files.
