# 01 — Wireless Network Requirements & Design

**Course:** CYB/360 — Wireless Security
**Deliverable:** Wireless Network Needs and Requirements
**Scenario:** International Plastics, Inc. (fictional manufacturing client)

## The scenario

Design a wireless LAN-to-LAN network for a manufacturing company's corporate campus. The network must support:

- High-density connectivity (large numbers of simultaneous devices)
- Multiple buildings across a campus (LAN-to-LAN bridging)
- Future scalability for new buildings
- Compliance with FCC regulations
- Strong security posture given client contractual obligations

## What I produced

A requirements and design document ([`Wireless_Network_Needs_and_Requirements.docx`](./Wireless_Network_Needs_and_Requirements.docx)) covering:

### Technical recommendations
- **Wi-Fi 6 (802.11ax)** access points for throughput and high-density efficiency
- **Wireless mesh topology** for redundancy, self-healing, and scalability — citing Cisco's Campus LAN/WLAN Solution Design Guide
- **WPA3-Enterprise** for encryption and authentication
- **Protected Management Frames (PMF)** to defend against deauthentication attacks
- **Role-based access control** to minimize lateral movement after a breach
- **SIEM integration** for real-time security monitoring

### Frequency band analysis

Comparison table covering 2.4 GHz, 5 GHz, and 6 GHz (Wi-Fi 6E) — strengths, weaknesses, and use cases for each. Key trade-offs:

- **2.4 GHz** — best range and penetration, but crowded and interference-prone
- **5 GHz** — higher throughput, less interference, but limited range
- **6 GHz (Wi-Fi 6E)** — newest, cleanest spectrum, but limited device support and higher infrastructure cost

### Compliance considerations
- FCC certification of all wireless equipment
- Operating within allocated frequency bands and power limits
- Recurring audits and firmware update cycles

## What this demonstrates

- **Standards-current design** — recommends Wi-Fi 6 and WPA3-Enterprise rather than legacy options
- **Architecture-first thinking** — mesh topology chosen for specific operational reasons (redundancy, scalability), not just because it's a buzzword
- **Defense in depth** — encryption + PMF + RBAC + SIEM is a layered approach, not a single control
- **Compliance as a baseline** — FCC compliance treated as a non-negotiable foundation, not an afterthought

## Key takeaway

The 2.4/5/6 GHz frequency analysis isn't just academic — it's the foundation for every real-world wireless design decision. Knowing when to deploy on which band (and why) is what separates someone who can configure a wireless network from someone who can architect one.
