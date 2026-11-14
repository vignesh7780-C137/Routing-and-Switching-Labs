# DHCP Configuration Lab

## Objective

Configure Dynamic Host Configuration Protocol (DHCP) so client devices receive IPv4 network settings automatically, then verify addressing and connectivity in Cisco Packet Tracer.

## Project artifact

Original Packet Tracer project: `Lemon DHCP project.pkt`

Repository target filename: `DHCP-Lab.pkt`

The Packet Tracer binary still needs to be added to this repository. The original project is retained separately; exact pool and addressing values are not inferred from the filename.

## Lab documentation

Record these details from the actual topology and configuration:

- DHCP server/router providing the leases
- DHCP pool name
- Network address and subnet mask
- Default gateway
- DNS server, if configured
- Excluded addresses or reserved ranges
- Client IP addresses and lease details

## Configuration reference

Typical Cisco IOS DHCP server structure (replace placeholders with values from the actual lab):

```text
enable
configure terminal
ip dhcp excluded-address <first-excluded-ip> <last-excluded-ip>
ip dhcp pool <pool-name>
 network <network-address> <subnet-mask>
 default-router <default-gateway>
 dns-server <dns-server-ip>
end
```

Only configure exclusions and DNS values that are required by the actual topology.

## Verification commands

On the Cisco IOS DHCP server/router:

```text
show ip dhcp pool
show ip dhcp binding
show ip dhcp server statistics
show running-config
```

On a Packet Tracer PC, use Desktop > IP Configuration and confirm that the assigned IP address, subnet mask, default gateway, and DNS settings match the intended network.

Connectivity checks:

```text
ipconfig
ping <default-gateway>
ping <destination-ip>
```

## Evidence checklist

- [ ] Packet Tracer topology screenshot
- [ ] DHCP pool configuration
- [ ] Excluded-address configuration, if used
- [ ] Client lease/IP Configuration screenshot
- [ ] Successful gateway ping
- [ ] Successful end-to-end connectivity test
- [ ] Packet Tracer `.pkt` project file

## Validation status

Documentation structure is in place. The actual pool name, network, subnet mask, gateway, lease assignments, and connectivity results must be transcribed from and verified against the original Packet Tracer project before being presented as completed results.
