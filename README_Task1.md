# 🔍 Task 1: Local Network Port Scanning & Packet Analysis

## 📌 Objective

To identify open ports and active devices on a local network using `Nmap`, and analyze the scanning behavior using `Wireshark`. This task builds foundational knowledge in network reconnaissance and traffic inspection.

---

## 🛠️ Tools Used

- **Nmap** – to perform TCP SYN scans (`-sS`) over a subnet
- **Wireshark** – to capture and analyze the SYN packets exchanged during the scan
- **Linux VM (VirtualBox with NAT)** – environment to run the scan
- **GitHub** – to submit the task artifacts

---

## ⏱️ Task Procedure

### 1. Installed Tools
```bash
sudo apt update
sudo apt install nmap wireshark
```

### 2. Identified Local IP Range
Used:
```bash
ip a
```
Result:
- IP Address: `10.0.2.5`
- Subnet Scanned: `10.0.2.0/24`

### 3. Ran the Nmap Scan
```bash
nmap -sS -v -oN vm_scan_results.txt 10.0.2.0/24
```

### 4. Captured Packets with Wireshark
- Started packet capture on interface (`eth0`)
- Ran the same scan while capturing
- Filtered traffic using:
  ```
  tcp.flags.syn == 1 && tcp.flags.ack == 0
  ```

---

## 📄 Files Submitted

| File Name                   | Description                                |
|----------------------------|--------------------------------------------|
| `Dharmiin Tank - Task 1.pdf` | Report or exported document (task summary) |
| `nmap_scan.txt`            | Hex dump or filtered output from Wireshark |
| `vm_scan_results.txt`      | Raw Nmap scan results in plain text         |

---

## 📊 Scan Results Summary

| Host IP     | Status | Open Ports | Notes                          |
|-------------|--------|-------------|--------------------------------|
| 10.0.2.5    | Up     | None        | All ports closed               |
| 10.0.2.3    | Up     | Filtered    | Likely VirtualBox NAT gateway  |
| All others  | Down   | –           | No response                    |

---

## 🔐 Observations & Risks

- **Open/filtered ports** reveal which services are exposed
- **NAT** limits device visibility from the external network
- **Filtered ports** often suggest firewall protection is active

---

## 📚 What I Learned

- How to scan subnets using Nmap TCP SYN scan (`-sS`)
- How SYN packets look in Wireshark (without ACK)
- The importance of port security and basic firewall behavior
- How scanning tools are used in both cybersecurity and ethical hacking

---

## 🚀 Credits

- Prepared by: **Dharmiin Tank**
- Task under: **Elevate Labs Cybersecurity Series**
- Date: _26 May 2025_