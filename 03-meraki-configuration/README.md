# 03 — Cisco Meraki Wireless Configuration

**Course:** CYB/360 — Wireless Security
**Deliverable:** Configure a Secure Wireless Network + WLAN Configuration Design Template
**Scenario:** Live configuration of 3 Cisco Meraki MR62 access points in an office WLAN

## The scenario

Configure three Cisco Meraki MR62 access points for an office space with documented antenna types and IP assignments:

- **WAP1** — `10.0.1.12` — Directional Beam Antenna
- **WAP2** — `10.0.1.14` — High-Gain Patch Antenna
- **WAP3** — `10.0.1.16` — Omni-Directional Antenna

For each AP, document the configuration changes, justify the choices, and explicitly identify the resulting vulnerabilities.

## What I produced

Two deliverables:

1. [`Configure_a_Secure_Wireless_Network.docx`](./Configure_a_Secure_Wireless_Network.docx) — per-AP configuration documentation with vulnerability analysis
2. [`WLAN_Configuration_Design_Template.docx`](./WLAN_Configuration_Design_Template.docx) — structured design template for the deployment
3. [`diagram_of_the_office_wireless_network.docx`](./diagram_of_the_office_wireless_network.docx) — network topology diagram

### Per-AP configuration approach

For each access point, the documentation captures:

- **Current setup** (frequency band the AP started on)
- **Change implemented** (frequency band switched to and why)
- **Vulnerability** (the security/performance trade-off introduced by the change)

For example, switching APs from 5 GHz to 2.4 GHz extends coverage but introduces:
- Higher exposure to interference from microwaves and Bluetooth devices
- Co-channel interference risk from overlapping neighbor networks
- Lower aggregate throughput

### Design template

The WLAN Configuration Design Template captures the full deployment as a reusable artifact — SSID strategy, security mode, channel assignments, AP roles, and topology references.

## What this demonstrates

- **Configuration-level competence** — not just "wireless networks should use WPA3," but actual per-device decisions with documented IPs, antenna types, and frequency selections
- **Honest trade-off analysis** — every change has a documented vulnerability. This is mature security thinking — recognizing that no change is "free."
- **Vendor familiarity** — Cisco Meraki is widely deployed in enterprise environments. Familiarity with Meraki's management model is directly applicable to real network admin and security roles.
- **Documentation discipline** — the design template format means another engineer could pick this up and continue the work without ambiguity

## Key takeaway

The most realistic part of this deliverable is that **every configuration change has a documented downside**. In real networks, security is always a balance — extending coverage usually weakens isolation, simplifying management often broadens attack surface. This deliverable shows I think about security in trade-offs, not absolutes.
