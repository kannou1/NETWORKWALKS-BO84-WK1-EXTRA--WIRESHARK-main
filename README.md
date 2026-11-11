# 🦈 Wireshark Network Security Lab
### By Dhia Kannou

<p align="center">
  <img src="https://img.shields.io/badge/Domain-Cybersecurity-blue?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Tool-Wireshark-1679A7?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Platform-Kali%20Linux-black?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Overall%20Score-100%25-brightgreen?style=for-the-badge" />
</p>

## 👨‍💻 Author

**Dhia Kannou**  
Cybersecurity Student | Network Security Enthusiast

## 📌 About This Project

This repository documents my hands-on practical exercises in **network traffic analysis and cybersecurity using Wireshark**.

Through six practical SOC labs, I explored network protocols, identified suspicious activities, reconstructed TCP conversations, detected authentication attacks, and investigated potential network security vulnerabilities.

## 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|---|---|
| Wireshark | Network packet capture and analysis |
| Kali Linux | Cybersecurity testing environment |
| VirtualBox | Virtual machine environment |
| TCP/IP | Network communication analysis |
| HTTP / FTP | Application protocol investigation |
| SIP / RTP | VoIP traffic analysis |

## 🎯 Objectives

- Understand packet capturing and network traffic analysis.
- Identify source and destination IP addresses.
- Analyse TCP flags and connection behaviour.
- Reconstruct TCP conversations using Follow TCP Stream.
- Identify security risks in unencrypted HTTP traffic.
- Detect suspicious FTP authentication attempts.
- Analyse SIP signalling and RTP media communication.
- Understand network security vulnerabilities and defensive techniques.

## 🔍 Wireshark Display Filters

| Investigation | Wireshark Filter |
|---|---|
| TCP SYN packets | `tcp.flags.syn == 1 && tcp.flags.ack == 0` |
| Specific IP address | `ip.addr == 192.168.10.66` |
| HTTP requests | `http.request` |
| FTP traffic | `ftp` |
| SIP signalling | `sip` |
| RTP media | `rtp` |

## 🧪 Practical Exercises

### Lab 03 — Identify the Attacker's IP

**Score: 100%**

**Objective:** Identify the suspected attacker IP address by analysing TCP SYN packets and recognising port scanning behaviour.

**Analysis:**
- Analysed a 309-packet capture.
- Identified 73 packets matching the SYN-focused filter.
- Suspected source IP: `192.168.10.66`.
- Target IP: `192.168.10.20`.
- Identified 40 probed ports.
- Open ports: 22, 80 and 443.

**Learning Outcome:** Recognised TCP SYN scanning behaviour by analysing IP addresses, destination ports and TCP flags.

**📸 Screenshot — Lab 03 | Dhia Kannou**

![Lab 3 Result](Lab%203%20Result%20-%20Dhia%20Kannou.png)

---

### Lab 04 — Follow TCP Stream

**Score: 100%**

**Objective:** Reconstruct and analyse application-level communication using Wireshark's Follow TCP Stream feature.

**Analysis:**
- Analysed a 246-packet capture.
- Investigated TCP port 5000.
- Identified TCP stream 5.
- Examined a 413-byte conversation between endpoints.
- Reconstructed TCP communication.

**Learning Outcome:** Learned to reconstruct TCP conversations and understand the confidentiality risks of unencrypted communication.

**📸 Screenshot — Lab 04 | Dhia Kannou**

![Lab 4 Result](Lab%204%20Result%20-%20Dhia%20Kannou.png)

---

### Lab 05 — Follow TCP Stream, Part 2

**Score: 100%**

**Objective:** Inspect HTTP responses and identify information exposed through client-side web content.

**Analysis:**
- Investigated the `/staff.html` request.
- Identified TCP stream 7.
- Observed an HTTP 200 response.
- Examined HTML content and comments.
- Identified information hidden in an HTML comment.

**Learning Outcome:** Learned to inspect HTTP responses and identify information exposed through web pages.

**📸 Screenshot — Lab 05 | Dhia Kannou**

![Lab 5 Result](Lab%205%20Result%20-%20Dhia%20Kannou.png)

---

### Lab 06 — HTTP Plain-Text Credentials

**Score: 100%**

**Objective:** Identify HTTP login submissions and understand the security risks of transmitting credentials without encryption.

**Analysis:**
- Analysed a 255-packet capture.
- Identified an HTTP POST request.
- Investigated the `/login` endpoint.
- Observed two login attempts.
- Examined plaintext HTTP traffic.

**Learning Outcome:** Identified the risks of transmitting authentication information over unencrypted HTTP and understood the importance of HTTPS.

**📸 Screenshot — Lab 06 | Dhia Kannou**

![Lab 6 Result](Lab%206%20Result%20-%20Dhia%20Kannou.png)

---

### Lab 07 — FTP Brute-Force Detection

**Score: 100%**

**Objective:** Detect suspicious FTP authentication attempts by analysing repeated login failures and successful responses.

**Analysis:**
- Analysed a 369-packet capture.
- Identified 24 FTP authentication failure responses (530).
- Observed a subsequent successful response (230).
- Investigated FTP control-channel communication.
- Recognised a pattern consistent with brute-force activity.

**Learning Outcome:** Learned to identify suspicious FTP authentication patterns using response codes and packet analysis.

**📸 Screenshot — Lab 07 | Dhia Kannou**

![Lab 7 Result](Lab%207%20Result%20-%20Dhia%20Kannou.png)

---

### Lab 08 — VoIP Call Analysis

**Score: 100%**

**Objective:** Analyse VoIP communication by identifying SIP signalling and RTP media traffic.

**Analysis:**
- Analysed a 1,051-packet capture.
- Identified SIP signalling packets.
- Examined RTP media traffic.
- Identified the PCMU audio codec.
- Explored Wireshark's RTP analysis tools.

**Learning Outcome:** Learned how SIP establishes and manages communication sessions while RTP carries real-time audio and video data.

**📸 Screenshot — Lab 08 | Dhia Kannou**

![Lab 8 Result](Lab%208%20Result%20-%20Dhia%20Kannou.png)

---

## 📊 Results Summary

| Lab | Practical Exercise | Score |
|:---:|---|:---:|
| 03 | Identify the Attacker's IP | 100% |
| 04 | Follow TCP Stream | 100% |
| 05 | Follow TCP Stream, Part 2 | 100% |
| 06 | HTTP Plain-Text Credentials | 100% |
| 07 | FTP Brute-Force Detection | 100% |
| 08 | VoIP Call Analysis | 100% |
| **Overall** | **6 Practical Exercises** | **100%** |

## 🏆 Key Learnings

- Network packet capture and inspection.
- TCP flags and port scanning detection.
- TCP stream reconstruction.
- HTTP request and response analysis.
- Plaintext credential exposure.
- FTP brute-force detection.
- SIP and RTP protocol analysis.
- Network security investigation techniques.

## 📝 Conclusion

These six Wireshark practical exercises provided valuable hands-on experience in network traffic analysis and cybersecurity investigation.

By analysing protocols such as TCP, HTTP, FTP, SIP and RTP, I strengthened my practical skills in packet inspection, identifying suspicious activities and understanding network security vulnerabilities.

This experience helped bridge the gap between theoretical networking knowledge and real-world cybersecurity analysis.

---

<p align="center">
  <b>🦈 Wireshark Network Security Lab</b><br/>
  <i>Developed and documented by Dhia Kannou</i><br/><br/>
  <img src="https://img.shields.io/badge/Completed-6%20Labs-success?style=flat-square" />
  <img src="https://img.shields.io/badge/Achievement-100%25-brightgreen?style=flat-square" />
</p>