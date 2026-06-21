# Comparative Security Analysis: Telnet vs. SSH

A practical, packet-level cybersecurity project demonstrating the critical role of cryptographic encapsulation in network security by auditing and exploiting clear-text protocol vulnerabilities.

---

## Project Overview
This project delivers a hands-on security comparison between **Telnet** and **Secure Shell (SSH)**. By capturing and analyzing live network traffic in a sandboxed environment, the project practically demonstrates how Telnet transmits data in plaintext—leaving it highly vulnerable to packet sniffing and credential harvesting—while SSH utilizes robust encryption to guarantee secure remote administration.

## Objectives
* **Service Architecture:** Deploy and configure active Telnet (`in.telnetd`) and OpenSSH (`sshd`) services within a Linux environment.
* **Traffic Auditing:** Intercept and evaluate live transit data packets using Wireshark.
* **Exploitation Simulation:** Simulate an on-path attacker sniffing network traffic to demonstrate plaintext credential exposure.
* **Cryptographic Verification:** Observe and validate the confidentiality of encrypted SSH packet payloads.
* **Comparative Analysis:** Document structural differences between secure and deprecated enterprise protocols.

## Tools & Technologies
* **Operating System:** Kali Linux
* **Services & Clients:** OpenSSH Server/Client, Telnet Server/Client
* **Network Analysis:** Wireshark Packet Analyzer
* **Protocol Layers:** TCP/IP Suite

---

## Methodology

### 1. Environment & Service Configuration
* Provisioned the target environment on Kali Linux, mapping out network interfaces and configuring hostnames.
* Initialized and secured the OpenSSH and Telnet daemon instances to handle incoming remote client connections.

### 2. Traffic Capture & Exploitation Simulation
* Initiated active packet sniffing sessions via Wireshark on the local network interface.
* Generated live network traffic by establishing a remote session over the Telnet client.
* Analyzed the captured stream to isolate and extract sensitive authentication credentials transmitted entirely in clear-text.

### 3. Cryptographic Validation
* Executed a parallel remote management session using the SSH client under active Wireshark surveillance.
* Inspected the resulting TCP payloads to verify that all data, including authentication vectors, remained heavily encrypted and resistant to passive interception.

---

## Comparative Analysis Results

| Feature | Telnet | SSH |
| :--- | :---: | :---: |
| **Data Encryption** | ❌ None | ✅ Encrypted |
| **Credential Security** | Plaintext (Vulnerable) | Cryptographically Secured |
| **Sniffing Resistance** | Low / Non-existent | High |
| **Industry Deployment** | Deprecated | Enterprise Standard |

---

## Key Takeaways
* **Protocol Insecurity:** Telnet lacks native confidentiality or integrity checks, making it fundamentally insecure for modern production networks.
* **Defensive Engineering:** SSH effectively mitigates credential-harvesting threats by ensuring end-to-end encryption, secure key exchange, and session integrity.
* **Encryption Imperative:** Packet-level auditing underscores why secure-by-default network architectures are an absolute requirement in modern cybersecurity.

## Conclusion
This analysis successfully provides concrete, packet-level evidence detailing why Telnet has been universally deprecated in favor of SSH for secure remote access. The findings emphasize that robust transport-layer encryption is a foundational prerequisite for protecting enterprise data assets.

---
**Author:** Amritesh Raj  
**Academic Specialization:** B.Tech Computer Science and Engineering (Cybersecurity)
