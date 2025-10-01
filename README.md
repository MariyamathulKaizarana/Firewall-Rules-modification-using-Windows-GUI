# Windows Firewall Experiment: GUI Rules for Port Management

## Overview
This repository demonstrates the use of **Windows Defender Firewall** through the GUI to manage inbound network traffic. The experiment focuses on creating, testing, and managing firewall rules to understand how traffic can be allowed or blocked based on ports.  

Key objectives: 
- Blocking insecure ports (Telnet, port 23)
- Allowing secure ports (SSH, port 22)
- Observing the behavior of firewall rules and testing connectivity

The task is purely for learning purposes and documenting hands-on experience with Windows firewall management.

---

## Tools
- **Operating System:** Windows 10
- **Firewall Tool:** Windows Defender Firewall with Advanced Security (GUI)
- **Ports Tested:**
  - Port 23 (Telnet) → Blocked
  - Port 22 (SSH) → Allowed

---

## Steps Performed

### 1. Open Firewall Configuration
- Opened **Run dialog** (`Win + R`) → typed `wf.msc` → pressed Enter  
- Opened Windows Defender Firewall with Advanced Security console  

### 2. List Existing Rules
- Navigated to **Inbound Rules** to see existing firewall rules  
- Observed default system rules (e.g., Remote Desktop, File and Printer Sharing)  

### 3. Block Telnet (Port 23)
- **New Rule…** → Port → TCP → 23 → Block the connection → Apply to Domain, Private, Public → Name: Block_Telnet  
- Verified rule appeared in inbound list  

### 4. Test Telnet Block
- Attempted connection to port 23 → blocked successfully  

### 5. Allow SSH (Port 22)
- **New Rule…** → Port → TCP → 22 → Allow the connection → Apply to Domain, Private, Public → Name: Allow_SSH  
- Verified rule appeared in inbound list  

### 6. Remove Test Rule
- Deleted **Block_Telnet** rule to restore previous state  

---

## Observations
- Blocking Telnet successfully prevented inbound connections on port 23.
- Allowing SSH explicitly permitted secure remote access on port 22.
- GUI firewall rules are easy to create, test, and remove.
- Windows Firewall acts as a filter for inbound/outbound traffic based on rules, direction, protocol, and port.

---

## Conclusion
This experiment demonstrates hands-on management of Windows firewall rules via GUI. It highlights the importance of blocking insecure ports and controlling network access, even on personal machines. The repository serves as a reference for future personal projects and learning about firewall configurations.

---

## Screenshots
- `screenshots/firewall_main_gui.png`  
- `screenshots/inbound_rules_before.png`  
- `screenshots/block_telnet.png`  
- `screenshots/allow_ssh.png`  
- `screenshots/inbound_rules_after.png`

---

## License
This repository is for personal learning purposes. Feel free to use the instructions for educational reference.
