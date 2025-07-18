# 🖧 Enterprise Network Simulation using Cisco Packet Tracer

This project is a practical simulation of a secure enterprise network designed in Cisco Packet Tracer. It demonstrates how core cybersecurity principles like network segmentation, firewall layering, DMZ implementation, and routing/NAT security are applied in a real-world scenario.

The network includes 3 user PCs, a database server, layered internal and external firewalls, a router, and a simulated internet connection (cloud). It highlights architectural flaws such as lack of segmentation and redundancy, while also suggesting improvements like VLANs, HSRP, Syslog integration, and port-level ACLs.

Ideal for beginners exploring Blue Team network defense, SOC design, or prepping for Cisco security certs.

---

## 🔧 Network Design Overview

This simulation includes:

- 🖥️ 3 User PCs (PC1–PC3)
- 🗄️ A Database Server (Server0)
- 🔥 Internal Firewall (Firewall1)
- 🌐 Router (Router0)
- 🔥 External Firewall (Firewall2)
- ☁️ Simulated Internet (Cloud)
- 🔀 A Switch (Switch0)

---

## Security Architecture Highlights

| Component | Purpose |
|----------|---------|
| **User PCs** | Client-side users accessing services |
| **Server0** | Internal database server |
| **Internal Firewall** | Controls east-west traffic |
| **Router** | Routes LAN to WAN traffic |
| **External Firewall** | DMZ isolation from Internet |
| **Cloud** | Simulates Internet access |

---

## IP Addressing Table

| Device / Interface | IP Address | Subnet Mask | Notes |
|--------------------|------------|-------------|-------|
| PC1                | 192.168.11.10 | 255.255.255.0 | Internal host |
| PC2                | 192.168.11.11 | 255.255.255.0 | Internal host |
| PC3                | 192.168.11.12 | 255.255.255.0 | Internal host |
| Server0            | 192.168.11.100 | 255.255.255.0 | DB server |
| Internal FW G0/0   | 192.168.11.1 | 255.255.255.0 | LAN-facing |
| Internal FW G0/1   | 192.168.22.1 | 255.255.255.0 | WAN-facing |
| Router G0/0        | 192.168.22.2 | 255.255.255.0 | LAN-facing |
| Router G0/1        | 192.168.28.2 | 255.255.255.0 | WAN-facing |
| External FW G0/0   | 192.168.28.1 | 255.255.255.0 | DMZ side |
| External FW G0/1   | 205.0.123.1  | 255.255.255.0 | Internet side |

---

## Observed Weaknesses

- No VLAN segmentation (flat Layer 2 design)
- No redundancy—single points of failure
- No logging/monitoring system
- Incomplete NAT/routing logic

---

## Suggested Improvements

- Implement VLANs (users, servers, management)
- Add HSRP or redundant firewalls
- Introduce dynamic routing (OSPF or EIGRP)
- Enable logging via Syslog or NetFlow
- Enforce tighter firewall ACLs
- DMZ isolation + port security

---

##  What I Learned

- The importance of firewall placement
- Why segmentation and monitoring matter
- How routing decisions impact security zones
- Layered defense in enterprise architecture

---


---

##  Contact

**Titus Patrick**  
`ptitus433@gmail.com` • [www.linkedin.com/in/patrick-titus-879613329](#) • 
