# Home Lab: Networking, Systems Administration & Cybersecurity
My hands-on journey into networking, Cisco, Windows administration, and cybersecurity.

# Project 01: TP-Link Router Connectivity Troubleshooting

## 1. Project Overview

**Project type:** Home networking lab  
**Device:** TP-Link TL-R470T+  
**Objective:** Connect a wired PC to the internet through a TP-Link router while preserving the existing Bell home internet connection.  
**Outcome:** Internet connectivity was restored successfully.

## 2. Lab Equipment

- Bell home internet gateway
- TP-Link TL-R470T+ multi-WAN router
- Windows PC connected through Ethernet
- Cisco router and Catalyst switch for future networking exercises
- ASUS RT-N66U wireless router for future lab use

## 3. Network Design

The initial lab connection used this layout:

```text
Internet
   |
Bell Home Gateway
   |
   | Ethernet
   v
TP-Link TL-R470T+
   |
   | Ethernet (LAN)
   v
Windows PC
```

The PC was configured to receive its network settings automatically through DHCP.

**Privacy note:** IP addresses and other identifying network details have been omitted from this public documentation.

## 4. Initial Problem

After connecting the Bell gateway to the TP-Link router and connecting the PC to the TP-Link LAN, the PC initially did not have internet access.

I accessed the TP-Link administration interface to inspect its network status and verify the basic configuration.

## 5. Troubleshooting Process

The troubleshooting process included:

1. Confirming the physical Ethernet connections between the Bell gateway, TP-Link router, and PC.
2. Reviewing the TP-Link WAN status and confirming that it reported a connected state with a dynamically assigned address.
3. Checking the TP-Link LAN configuration and DHCP settings.
4. Using Windows network information to verify the PC's IPv4 configuration, subnet mask, and default gateway.
5. Continuing troubleshooting until internet connectivity was restored.

*Note: This summary records the checks and outcome I can confirm. I have not documented an unverified root cause or claimed specific ping or DNS test results.*

## 6. Final Result

**Status: Resolved**

The PC can access the internet through the TP-Link router. The existing Bell internet connection remains in use.

## 7. What I Learned

- How to connect a secondary router behind a home internet gateway.
- The difference between WAN and LAN connections.
- How DHCP provides network settings to a client device.
- How to inspect IPv4 configuration and the default gateway in Windows.
- Why troubleshooting should proceed systematically, from physical connections to network configuration.
- Why documenting the problem, diagnostic steps, and final result is useful for future troubleshooting.

## 8. Next Steps

- Create a simple network diagram with sanitized labels.
- Practise basic connectivity tests, including gateway reachability, external IP connectivity, and DNS resolution.
- Connect to the Cisco router using the console cable.
- Build isolated Cisco routing and switching exercises.
- Document each future lab with screenshots that do not expose sensitive information.

## 9. Security and Privacy

This project intentionally excludes Wi-Fi passwords, router administration credentials, public IP addresses, serial numbers, and personal network identifiers.

Any screenshots or configuration examples published with this project should be reviewed and sanitized before uploading.
