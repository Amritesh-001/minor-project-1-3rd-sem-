                           **Minor 1 Project Report**

**Name:** Amritesh Raj  
**Course:** B.Tech CSE (Cyberscurity)  
**Project Title: Comparative Security Analysis of Telnet and SSH**

### **Overview**

This project presents a practical security comparison between Telnet and SSH by capturing and analyzing live network traffic using Wireshark. It demonstrates how Telnet transmits data in plaintext, making it vulnerable to sniffing attacks, while SSH encrypts all communication to ensure secure remote access.

### **Objectives**

* Configure Telnet and SSH services on Kali Linux  
* Capture and analyze Telnet and SSH traffic using Wireshark  
* Demonstrate plaintext credential exposure in Telnet  
* Observe encrypted communication in SSH  
* Perform a comparative security analysis

### **Tools & Technologies**

* Kali Linux  
* Telnet (in.telnetd)  
* OpenSSH (sshd)  
* Wireshark  
* Telnet Client  
* SSH Client

### **Methodology (Summary)**

1. Configure hostname and services on Kali Linux  
2. Capture Telnet traffic and analyze plaintext credentials  
3. Capture SSH traffic and observe encrypted packets  
4. Simulate an attacker sniffing network traffic  
5. Compare security properties of Telnet and SSH

### **Results**

| Feature | Telnet | SSH |
| :---- | :---- | :---- |
| Encryption | ❌ No | ✅ Yes |
| Credential Security | Plaintext | Encrypted |
| Resistance to Sniffing | Low | High |
| Usage Status | Deprecated | Industry Standard |

### **Key Takeaways**

* Telnet is insecure and should not be used in modern networks  
* SSH provides confidentiality, integrity, and secure authentication  
* Encryption is critical for protecting network communications

### **Conclusion**

The project clearly demonstrates why Telnet is deprecated and why SSH is universally adopted for secure remote access. Packet-level analysis provides strong evidence of the importance of encryption in cybersecurity.

