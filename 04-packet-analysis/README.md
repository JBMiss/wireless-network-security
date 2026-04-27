# 04 — Wireless Packet Capture Analysis

**Course:** CYB/360 — Wireless Security
**Deliverable:** Packet Capture Analysis report
**Scenario:** Threat-rank and analyze five wireless PCAP samples for management briefing

## The scenario

Given five real-world wireless packet captures, produce a management-facing report that:

1. Ranks each capture by threat severity
2. Describes the traffic
3. Identifies the risk
4. Recommends countermeasures
5. Explains the rationale for the rankings

## What I produced

A packet capture analysis report ([`Packet_Capture_Analysis.docx`](./Packet_Capture_Analysis.docx)) structured as a memo to management with:

### Threat ranking table

| # | Capture | Traffic Type | Risk |
|---|---|---|---|
| 1 | `wap_google.pcap` | Wireless Session Protocol gateway | DoS attacks targeting availability |
| 2 | `ciscowl.pcap.gz` | Cisco WLCCP control protocol | Man-in-the-Middle via open ports |
| 3 | `nb6-hotspot.pcap` | DNS/TLS/PPP/ARP — community wireless | Eavesdropping on public hotspot traffic |
| 4 | `wpa-eap-tls.pcap.gz` | WPA-EAP/Rekey | Key compromise → data exposure |
| 5 | `wpa-Induction.pcap.gz` | WPA EAPOL handshake | DoS + KRACK attack vectors |

For each ranked capture, the report includes a traffic description, risk description, and recommended countermeasures (firewall rules, encryption, port hardening, etc.).

### Methodology sections

The report also covers:

- **Distinguishing hostile from normal packet data** — using DSCP, TTL, and flag values as forensic indicators of suspicious routing paths
- **Recognizing attack signatures** — for example, regularly-spaced repeated DNS requests as a possible C2 beacon signal
- **Context-driven analysis** — what's anomalous in one network is normal in another; baseline knowledge is essential
- **Privacy/inspection trade-offs** — packet payload inspection finds threats but raises privacy considerations

## What this demonstrates

- **Threat hunting from raw traffic** — not just "use Wireshark" but actually analyzing real captures and extracting findings
- **Communication for non-technical audiences** — the memo format translates technical threats into management-readable risk language
- **Familiarity with common wireless attacks** — DoS, MitM, KRACK, EAPOL replay, deauthentication
- **Forensic mindset** — using header fields like DSCP and TTL as investigation hooks, not just descriptive metadata

## Key takeaway

The strongest part of this report is the rationale section: each threat ranking is justified, not declared. A reader can see *why* the EAPOL handshake capture is ranked highest (KRACK exposure + DoS surface) rather than just being told it is. That's the difference between a security analyst and someone who memorized a threat list.
