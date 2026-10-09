# Home Lab: Networking, Systems Administration & Cybersecurity
My hands-on journey into networking, Cisco, Windows administration, and cybersecurity.


## Project Overview

Welcome to my home lab! This repository documents my hands-on learning journey in computer networking, Cisco technologies, Windows administration, and cybersecurity.

My goal is to build practical technical skills through real-world configurations, troubleshooting exercises, and documented projects while maintaining the stability of my existing home internet connection.

## Learning Objectives

- **Networking:** Understand IPv4 addressing, subnetting, DHCP, DNS, routing, and network troubleshooting.
- **Cisco & CCNA:** Practise router and switch configuration, console access, VLANs, and network management.
- **Windows Administration:** Explore Windows 11 Pro, Active Directory, users, groups, and Group Policy.
- **Microsoft Cloud Administration:** Learn Microsoft 365 and Microsoft Entra ID fundamentals.
- **Cybersecurity:** Practise access control, network security, system hardening, and security analysis.
- **Documentation:** Record configurations, troubleshooting steps, results, and lessons learned using GitHub.

## Current Lab Equipment

| Equipment | Purpose | Status |
|---|---|---|
| Bell internet gateway | Provides the existing home internet connection | Working |
| TP-Link TL-R470T+ | Router and networking experiments | Connected; internet access restored |
| Cisco router | Cisco IOS and routing practice | Planned |
| Cisco Catalyst 2950 switch | Switching and VLAN practice | Planned |
| Intel NUC 7i7DNK1E | Compact Windows administration and lab host | Working |
| ASUS RT-N66U | Potential wireless access point | Working |
| Console cable | Connect to Cisco equipment for configuration | Available, setup pending |

## Network Topology

My initial working configuration uses the Bell gateway and TP-Link router. The Cisco equipment will be incorporated into the lab in a later phase.

```text
                 Internet
                    |
            Bell Internet Gateway
                    |
                 Ethernet
                    |
             TP-Link TL-R470T+
                    |
                 Ethernet
                    |
                Lab PC
```

### Current Network Configuration

| Setting | Value |
|---|---|
| Bell gateway address | 192.168.2.1 |
| TP-Link WAN address | 192.168.2.70 |
| TP-Link LAN address | 192.168.0.1 |
| TP-Link subnet mask | 255.255.255.0 |
| Lab PC IPv4 address | 192.168.0.187 |
| Lab PC default gateway | 192.168.0.1 |
| TP-Link WAN connection type | Dynamic IP |
| TP-Link DHCP server | Enabled |

*Note: These are the addresses observed during my initial setup. They may change if DHCP leases or network settings change.*

## Project 01: TP-Link Router Internet Connectivity Troubleshooting

### Objective

Connect the TP-Link TL-R470T+ to my existing Bell gateway and restore internet access to my lab PC without disrupting the existing home network.

### Initial Setup

1. Connected the Bell gateway's LAN port to WAN1 on the TP-Link router.
2. Connected the TP-Link router's LAN port to my lab PC.
3. Accessed the TP-Link administration interface to inspect its network settings.
4. Checked the WAN connection status and the PC's IPv4 configuration.
5. Troubleshot the connectivity issue until internet access was restored.

### Observations

The TP-Link router showed a WAN address of `192.168.2.70`, a gateway of `192.168.2.1`, and a LAN address of `192.168.0.1`.

The PC received the IPv4 address `192.168.0.187` with subnet mask `255.255.255.0` and default gateway `192.168.0.1`.

### Outcome

**Status: Resolved.**

Internet access through the TP-Link router is working. The exact cause of the original connectivity issue has not yet been confirmed, so I will document further diagnostic findings if I reproduce or investigate it again.

### Lessons Learned

- How to inspect WAN and LAN settings on a router.
- How to read IPv4 address, subnet mask, and default gateway information using Windows.
- How to distinguish the upstream gateway network (`192.168.2.0/24`) from the TP-Link LAN network (`192.168.0.0/24`).
- Why it is important to preserve a working home network while building a lab.

## Planned Projects

- [ ] Document the initial network troubleshooting in greater detail.
- [ ] Connect to the Cisco router using the console cable.
- [ ] Inspect the Cisco router and Catalyst switch configurations.
- [ ] Practise IPv4 addressing and subnetting.
- [ ] Configure VLANs and inter-VLAN routing where supported.
- [ ] Set up the Intel NUC for Windows administration practice.
- [ ] Build an Active Directory lab.
- [ ] Explore Microsoft 365 and Microsoft Entra ID.
- [ ] Complete networking and cybersecurity troubleshooting exercises.
- [ ] Add network diagrams, command outputs, and lessons learned to each project.

## Documentation Principles

For each lab, I aim to document:

1. **Objective** — What I want to accomplish.
2. **Environment** — Equipment, operating systems, and network topology.
3. **Configuration** — Settings and commands used.
4. **Troubleshooting** — Symptoms, diagnostic steps, and findings.
5. **Results** — What worked, what did not, and how the outcome was verified.
6. **Lessons learned** — What I would improve or investigate next.

This repository is a work in progress and reflects my practical learning journey.
