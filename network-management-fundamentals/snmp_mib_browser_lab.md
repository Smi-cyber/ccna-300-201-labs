# Lab: SNMP Monitoring & MIB Management in Cisco Packet Tracer

## 🎯 Objectives
- Configure SNMP read-only (RO) and read-write (RW) community strings on Cisco routers.
- Use a simulated PC MIB browser tool to poll device metrics (interfaces, routing table, OSPF stats).
- Modify device parameters (router hostname) remotely via SNMP Write access.

## 🛠️ Topology Summary
- **Devices:** Router 1 (R1), Router 2 (R2), and an Administration PC running the MIB Browser tool.
- **Protocol:** SNMPv2c with community strings (`public` for Read, `private` for Write).

## 💻 Router Configuration Snippets
Applied on both R1 and R2 via CLI:

```cisco
enable
configure terminal
! Enable SNMP Read-Only and Read-Write communities
snmp-server community public ro
snmp-server community private rw

! Optional Metadata
snmp-server contact Network_Admin_Isaac
snmp-server location Lab_Core_Rack