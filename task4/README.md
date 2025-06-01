# Task 4: Firewall Setup and Testing using UFW on Linux

This task involves configuring and testing basic firewall rules on Linux using UFW (Uncomplicated Firewall) to allow or block specific network traffic.

---

## Tools Used  
- Operating System: Kali Linux  
- Firewall: UFW (Uncomplicated Firewall)  
- Services Tested: Telnet (port 23), SSH (port 22)  

---

## Steps Performed

| Step | Description                                 | Command / Output                                     |
|-------|---------------------------------------------|----------------------------------------------------|
| 1     | Started necessary services                   | ```bash<br>sudo systemctl start redis-server<br>``` |
| 2     | Enabled UFW firewall                         | ```bash<br>sudo ufw enable<br>```                   |
|       |                                             | Output:<br>```Firewall is active and enabled on system startup``` |
| 3     | Listed current firewall rules                | ```bash<br>sudo ufw status numbered<br>```          |
| 4     | Blocked inbound traffic on Telnet port (23) | ```bash<br>sudo ufw deny 23<br>```                   |
|       |                                             | Output:<br>```Rule added```                          |
| 5     | Tested Telnet connection on port 23 (fail)  | ```bash<br>telnet localhost 23<br>```                |
|       |                                             | Output:<br>```Connection refused```                  |
| 6     | Allowed SSH port (22) traffic                 | ```bash<br>sudo ufw allow 22<br>```                   |
|       |                                             | Output:<br>```Skipping adding existing rule```       |
| 7     | Removed the Telnet block rule                 | ```bash<br>sudo ufw delete deny 23<br>```             |
|       |                                             | Output:<br>```Rule deleted```                         |
| 8     | Verified final firewall rules                 | ```bash<br>sudo ufw status verbose<br>```             |

---

## Summary  
UFW provides a user-friendly interface to manage firewall rules. It filters network traffic based on ports and protocols. In this task, we blocked Telnet (port 23) traffic to prevent unauthorized access and ensured SSH (port 22) was allowed for remote connections. Testing confirmed that the block was effective, and the firewall rules were later restored to their original state.

---

## Additional Notes  
- Telnet is an insecure protocol and should be blocked in most environments.  
- SSH is widely used for secure remote management, hence kept allowed.  
- UFW simplifies managing complex iptables rules with straightforward commands.  

---

## Files Included  
- `firewall_rules.txt` - Snapshot of the final firewall configuration.

---

**Stay secure by properly managing your firewall!**
