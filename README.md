# Wireless Network Security — Design, Deployment & Analysis

> A complete wireless security project covering enterprise network design, residential site survey, Cisco Meraki configuration, and packet capture analysis. Demonstrates end-to-end thinking from requirements gathering through threat hunting.

**Author:** Jesse Missaghian
**Program:** B.S. in Cybersecurity, University of Phoenix
**Course:** CYB/360 — Wireless Security
**Timeline:** November 2023 – January 2024

---

## What this project is

A multi-phase wireless security project covering **three different deployment scenarios** to demonstrate breadth of wireless security skills:

1. **Enterprise WLAN design** — designing a wireless LAN-to-LAN network for a fictional manufacturer's corporate campus
2. **Residential site survey** — assessing and recommending a secure home wireless network for a multi-story home with 10+ devices
3. **Live Meraki configuration** — configuring three Cisco Meraki MR62 access points with documented vulnerability tradeoffs

The project closes with a **packet capture analysis** assessing five real-world wireless captures for threats and defensive countermeasures, plus a final **executive presentation** synthesizing the security configurations.

## Why this matters for a security role

Wireless networks are one of the most common attack surfaces — and one of the most often misconfigured. This project demonstrates:

1. **Requirements-driven design** — translating business needs (high-density manufacturing campus, multi-tenant residential) into specific technical specifications (WPA3-Enterprise, mesh topology, AP placement, frequency band selection)
2. **Real configuration work** — not just describing wireless security, but actually configuring Cisco Meraki APs with documented frequency, antenna, and channel decisions
3. **Threat analysis from raw traffic** — reading PCAPs and identifying attack signatures, not just reading about them
4. **Trade-off awareness** — every configuration decision in this project has documented vulnerabilities (e.g., switching to 2.4 GHz for coverage at the cost of interference exposure)

## The five deliverables

| # | Deliverable | What it covers |
|---|---|---|
| [01](./01-requirements-and-design) | **Requirements & Design** | Enterprise WLAN design for International Plastics, Inc. — Wi-Fi 6, mesh topology, FCC compliance, WPA3-Enterprise, frequency band analysis |
| [02](./02-site-survey) | **Residential Site Survey** | Multi-story home network assessment — dead zone mapping, RF interference identification, AP placement recommendations |
| [03](./03-meraki-configuration) | **Cisco Meraki Configuration** | Live configuration of 3 Meraki MR62 APs with WLAN design template — frequency, antenna, and channel tradeoffs documented |
| [04](./04-packet-analysis) | **Packet Capture Analysis** | Threat ranking and analysis of 5 wireless PCAPs — DoS, MitM, KRACK, EAPOL handshake attacks, with countermeasure recommendations |
| [05](./05-presentation) | **Security Configurations Briefing** | Executive presentation synthesizing the wireless security recommendations |

## Technical concepts covered

- **Wireless standards:** 802.11ax (Wi-Fi 6), Wi-Fi 6E (6 GHz), 2.4/5/6 GHz frequency band tradeoffs
- **Security protocols:** WPA3-Enterprise, Protected Management Frames (PMF), EAP-TLS, role-based access control
- **Network design:** mesh topology, AP placement, channel planning, high-density deployment
- **Threat analysis:** DoS attacks, Man-in-the-Middle, KRACK, deauthentication attacks, EAPOL key reinstallation
- **Tools & vendors:** Cisco Meraki MR62, Wireshark/tcpdump (PCAP analysis), SIEM integration concepts
- **Compliance:** FCC frequency/power regulations, audit/firmware update cycles

## How to read this repo

**If you have 5 minutes:** read this README and skim [`01-requirements-and-design`](./01-requirements-and-design) — sets the scenario.

**If you have 15 minutes:** add [`03-meraki-configuration`](./03-meraki-configuration) and [`04-packet-analysis`](./04-packet-analysis) — these are the most technically substantive.

**If you have 30 minutes:** read all five in order.

---

## About me

Cybersecurity professional based in Fresno, CA, completing my B.S. in Cybersecurity at University of Phoenix and CompTIA Security+ certified. Open to roles in cybersecurity — analyst, SOC, pen testing, network security.

- 🐙 [GitHub: @JBMiss](https://github.com/JBMiss)
- 💼 [LinkedIn: Jesse Missaghian](https://www.linkedin.com/in/jesse-missaghian-b77b4516a)
