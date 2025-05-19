# IOC 13 – ARP Spoofing Case Study

This project provides a forensic walkthrough of a real-world network redirection technique using ARP spoofing. It highlights the challenges of detecting unauthorized Layer 2 manipulation from a host perspective and demonstrates how attackers exploit trust and stateless protocols to intercept traffic, harvest credentials, and reroute communications within local networks.

## Overview

The case study centers on a hostile actor who has already gained access to a local subnet and proceeds to execute an Address Resolution Protocol (ARP) spoofing attack. This mid-stage maneuver involves broadcasting forged ARP replies to mislead nearby hosts about the legitimate MAC address associated with a critical IP (e.g., gateway or DNS server). This tactic positions the attacker as a man-in-the-middle, enabling credential theft, session hijacking, and lateral movement.

## Key Topics Covered

- **How ARP functions at OSI Layer 2 and why it’s vulnerable**
- **The role of operating system behavior in enabling packet-level deception**
- **Use of promiscuous mode and raw socket manipulation**
- **Triage techniques for identifying ARP-related anomalies from host systems**
- **Forensic linkage between process execution, network interfaces, and malicious behavior**

## Investigative Breakdown

This project follows a structured triage format:

- **Telemetry Sources**: PCAP, NetFlow, Windows Event Logs, Volatile Memory
- **Host-Based Detection Techniques**: Process analysis, EDR inspection, registry and memory review
- **Cross-Layer Mapping**: From credential theft to execution, background persistence, and interface-level activity
- **OSI Model Integration**: Focused on Layer 2 exploitation with implications at Layers 3 and 7
- **Defender Response Strategy**: ARP table validation, Wireshark filtering, gateway integrity checks, switch-level enforcement using Dynamic ARP Inspection (DAI)

## Educational Value

This analysis is designed to reinforce structured cybersecurity thinking:

- Understand how attacks unfold **inside** a network, after initial compromise
- Learn to **map attacker behavior** to observable host and network signals
- Strengthen your command of **forensic triage tools and methods**
- See how operating system layers interact with low-level protocols like ARP

## Files

- `ioc13-arp-spoofing.ipynb`: Full case study notebook with embedded technical explanations and strategic commentary

## License

This project is open source and available for educational and defensive research purposes. Attribution encouraged.
