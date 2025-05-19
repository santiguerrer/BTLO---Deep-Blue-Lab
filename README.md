# 🧠 BTLO – Deep Blue Lab

**Platform:** [Blue Team Labs Online](https://blueteamlabs.online/)  
**Category:** Incident Response / Threat Hunting  
**Tools Used:** DeepBlueCLI, PowerShell, Windows Event Viewer  
**Link:** [Deep Blue Investigation](https://blueteamlabs.online/home/investigation/32)

---

## 📝 Overview

In the **Deep Blue** lab, I conducted a forensic investigation on Windows event logs to detect and analyze signs of a security incident. The focus was on identifying RDP access, command execution, malicious service creation, and privilege escalation — common techniques used in real-world attacks.

---

## 🔍 Key Findings

### 🔸 Suspicious User Activity
Identified that the user account `Mike Smith` executed `GoogleUpdate.exe`, an unusual binary in this context.

### 🔸 Meterpreter Payload Execution
Meterpreter activity was detected at `2021-04-10 10:48:14`, suggesting post-exploitation control over the system.

### 🔸 Malicious Service Created
A suspicious service named `rztbzn` was created, likely used to establish persistence.

### 🔸 Malicious File Execution
The attacker downloaded and executed `serviceupdate.exe`, a suspected payload used for remote access.

### 🔸 Unauthorized User Created
A new local user `ServiceAct` was created using:
```bash
net user ServiceAct /add
