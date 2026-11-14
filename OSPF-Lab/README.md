# OSPF Configuration Lab

## Objective

Configure and verify dynamic routing between Cisco routers using Open Shortest Path First (OSPFv2) in Cisco Packet Tracer.

## Project artifact

Original Packet Tracer project: `Lemon ospf configuration model.pkt`

Repository target filename: `OSPF-Lab.pkt`

The Packet Tracer binary still needs to be added to this repository. The original project is retained separately; no topology or configuration values are inferred from the filename.

## Lab documentation

Record these details from the actual topology before treating the lab as fully documented:

- Router names and topology
- Interface names and IPv4 addresses
- Subnet masks and connected networks
- OSPF process ID and area assignments
- Router IDs, if manually configured
- Neighbor adjacency state
- OSPF-learned routes
- End-to-end connectivity test results

## Configuration reference

Typical Cisco IOS OSPF configuration structure (replace placeholders with values from the actual lab):

```text
enable
configure terminal
router ospf <process-id>
 router-id <router-id>
 network <network-address> <wildcard-mask> area <area-id>
end
```

Do not copy placeholder values directly into a device. Configure each router according to its own interfaces and addressing plan.

## Verification commands

```text
show ip interface brief
show ip ospf
show ip ospf neighbor
show ip route ospf
show ip protocols
ping <destination-ip>
```

## Evidence checklist

- [ ] Packet Tracer topology screenshot
- [ ] Router interface addressing
- [ ] OSPF configuration from each router
- [ ] OSPF neighbor adjacency output
- [ ] OSPF routing-table output
- [ ] Successful end-to-end ping evidence
- [ ] Packet Tracer `.pkt` project file

## Validation status

Documentation structure is in place. Actual addressing, OSPF parameters, neighbor state, and ping results must be transcribed from and verified against the original Packet Tracer project before being presented as completed results.
