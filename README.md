# CCNA Lab 06 - DHCP

## Project Overview

This lab demonstrates how DHCP automatically assigns IP addresses and network configuration to devices using a Cisco router as a DHCP server in Cisco Packet Tracer.

---

## Objectives

- Understand how DHCP works
- Configure a Cisco router as a DHCP server
- Create a DHCP pool
- Configure excluded IP addresses
- Automatically assign IP addresses to client devices
- Verify DHCP leases and network connectivity

---

## Tools

- Cisco Packet Tracer
- GitHub
- Markdown

---

##  Network Topology

![Network Topology](images/Topology.png)

---

##  Network Configuration

**Network:** `192.168.1.0/24`  
**Default Gateway:** `192.168.1.1`  
**DNS Server:** `8.8.8.8`  
**Excluded Addresses:** `192.168.1.1 - 192.168.1.9`

### DHCP Assigned Addresses

- PC0 → `192.168.1.10`
- PC1 → `192.168.1.11`
- PC2 → `192.168.1.12`

---

##  Configuration Steps

1. Configured the router interface with `192.168.1.1/24`.
2. Enabled the router interface using `no shutdown`.
3. Excluded addresses from `192.168.1.1` to `192.168.1.9`.
4. Created a DHCP pool named `LAN`.
5. Configured the network as `192.168.1.0/24`.
6. Configured `192.168.1.1` as the default gateway.
7. Configured `8.8.8.8` as the DNS server.
8. Configured all PCs to obtain their network settings using DHCP.
9. Verified DHCP leases using `show ip dhcp binding`.
10. Tested network connectivity using the `ping` command.

---

## DHCP Process - DORA

DHCP uses four main steps to assign an IP address:

1. **Discover** - The client searches for a DHCP server.
2. **Offer** - The DHCP server offers an available IP address.
3. **Request** - The client requests the offered IP address.
4. **Acknowledge** - The DHCP server confirms the lease.

---

##  Test Results

The router successfully assigned IP addresses to all three PCs using DHCP.

- PC0 received `192.168.1.10`
- PC1 received `192.168.1.11`
- PC2 received `192.168.1.12`

The DHCP bindings were successfully verified on the router, and connectivity between the devices and the default gateway was tested using `ping`.

**Result:** DHCP configuration and network connectivity were successful.

---

## Skills Learned

- DHCP configuration
- DHCP pools
- DHCP excluded addresses
- Dynamic IP addressing
- DHCP DORA process
- Cisco IOS CLI
- DHCP lease verification
- Connectivity testing

---

##  Project Files

- [Packet Tracer File](Packet-tracer/dhcp-lab.pkt)
- [Network Topology](image/Topology.png)

---

##  Author

**Kawthar Bader**

Computer Networks Student | CCNA Learner | Building Networking Labs

---
