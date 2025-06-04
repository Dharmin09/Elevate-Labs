# Task 5: Capture and Analyze Network Traffic Using Wireshark

## 🎯 Objective
Capture live network packets on a Linux VM using Wireshark and identify basic protocols and traffic types.

---

## 🛠 Tools Used
- **Wireshark** (Graphical packet analyzer)
- **Linux VM on VirtualBox**
- **ping**, **dig**, and basic web browsing to generate traffic

---

## 📋 Steps Performed

1. **Installed Wireshark** on Linux VM using `sudo apt install wireshark`.
2. **Launched Wireshark** and selected the active network interface (`enp0s3`).
3. **Started packet capture** and generated traffic using:
   - `ping google.com`
   - DNS lookups and web access
4. **Stopped the capture** after ~1 minute.
5. **Applied filters** in Wireshark to analyze protocols:
   - `dns`, `icmp`, `dhcp`, `arp`
6. **Exported** the packet capture as `task5_capture.pcap`.
7. **Analyzed and documented** the findings in the report.

---

## 🔍 Protocols Identified

| Protocol | Purpose                          | Description |
|----------|----------------------------------|-------------|
| **DHCP** | IP Assignment                    | Observed complete DHCP handshake: Discover, Offer, Request, ACK. |
| **DNS**  | Domain Name Resolution           | Resolved `google.com` to IPv4 and IPv6 addresses, and performed reverse PTR lookup. |
| **ICMP** | Network Connectivity Testing     | Sent multiple Echo Requests (ping) to `google.com` and received valid Echo Replies. |
| **ARP**  | MAC Address Resolution           | Translated gateway IP `10.0.2.1` to MAC address via ARP request/reply. |

---

## 📁 Output Files

- `task5_capture.pcap`: Raw packet capture file.
- `wireshark_report.md`: Protocol summary and findings (this document).

---

## 📌 Outcome

This task provided practical experience in:
- Capturing real-time network traffic using Wireshark
- Identifying and understanding key networking protocols
- Analyzing packets using protocol filters and timestamps

---

## 🧠 Author
**Dharmin Tank**  
B.Tech CSE (Cybersecurity), 3rd Year  
NMIMS MPSTME  
