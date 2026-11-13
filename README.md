# Network Troubleshooting Lab

Hands-on lab for practicing enterprise network troubleshooting across VLANs, inter-VLAN routing, DHCP, DNS, and switching. Each scenario documents symptom → diagnosis → root cause → fix → verification, with topology files and screenshots for reproducibility.

## Environment
- **Simulator:** Cisco Packet Tracer
- **Devices:** Cisco WS-C3560 (L3), WS-C2960-24TT-L (L2), end-host PCs
- **Tools:** IOS `show`/`debug` commands, `ping`, `traceroute`, `ipconfig`

## Scenarios

| ID  | Scenario | Technologies | Status |
|-----|----------|--------------|--------|
| 001 | [Inter-VLAN routing failure from trunk allowed-VLAN misconfig](scenarios/001-trunk-allowed-vlan.md) | VLAN, 802.1Q, SVI | ✅ |
| 002 | [DHCP client gets IP but cannot route off-subnet](scenarios/002-dhcp-wrong-gateway.md) | DHCP, SVI | ✅ |
| 003 | DNS resolution failure | DNS, ACL | ⏳ |

## Repository structure

    topologies/   Packet Tracer files + topology screenshots per scenario
    scenarios/    Markdown write-up for each scenario

## How to reproduce
1. Install Cisco Packet Tracer (v8.x or later)
2. Open the `.pkt` file for the scenario under `topologies/<scenario>/`
3. Follow the diagnostic steps in `scenarios/<NNN>-*.md`

## Notes
Self-directed lab — every scenario is intentionally broken, diagnosed, documented, and fixed.
