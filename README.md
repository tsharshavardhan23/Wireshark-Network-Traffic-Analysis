# Wireshark-Network-Traffic-Analysis
Task-3
# 🔐 Wireshark Network Traffic Analysis

## 📌 Project Overview

This project demonstrates hands-on network traffic analysis using **Wireshark**.

The objective was to capture and analyze real network packets and understand how common protocols such as **TCP, DNS, and HTTP** operate at the packet level.

The project also included analysis of TCP behavior and Wireshark's built-in packet analysis indicators.

---

## 🎯 Objectives

- Understand TCP communication at the packet level
- Analyze the TCP three-way handshake
- Capture and analyze DNS queries and responses
- Analyze HTTP request and response traffic
- Examine TCP sequence information
- Identify unusual TCP conditions reported by Wireshark
- Develop practical packet-analysis skills

---

## 🛠️ Tools Used

| Tool | Purpose |
|------|---------|
| Wireshark | Network packet capture and analysis |
| Windows | Analysis environment |
| Web Browser | Generate network traffic |
| PowerShell | Generate HTTP traffic |

---

## 🔎 Analysis Performed

### 1. TCP Three-Way Handshake

Analyzed the TCP connection establishment process:

```text
SYN
 ↓
SYN/ACK
 ↓
ACK
2. DNS Traffic Analysis

Captured and analyzed DNS queries and responses.

The analysis included:

DNS queries
DNS responses
Domain names
UDP communication
Port 53

Evidence: 02_DNS_Analysis.png

3. HTTP Traffic Analysis

Captured an HTTP request and examined the corresponding server response.

Example request:

GET / HTTP/1.1

Example response:

HTTP/1.1 200 OK

The analysis demonstrated the HTTP request-response communication model.

Evidence:

03_HTTP_GET.png
04_HTTP_200_OK.png
4. TCP Analysis

Wireshark's TCP analysis features were used to examine TCP sequence behavior and identify unusual conditions in the captured traffic.

A tcp.analysis.lost_segment indication was observed during analysis.

Note: A Wireshark lost-segment indication does not by itself prove that an actual network packet was lost. It can also result from packets missing from the capture or other capture conditions.

Evidence: 05_TCP_Anomaly.png

📊 Key Findings
Area	Observation
TCP	Three-way handshake successfully identified
DNS	Queries and responses observed
HTTP	GET request and 200 OK response captured
TCP Analysis	Lost-segment indication observed
Packet Analysis	Protocol behavior examined at packet level
📚 What I Learned

Through this project, I gained practical experience in:

Reading packet captures
Understanding TCP flags
Identifying SYN, SYN/ACK and ACK packets
Understanding DNS communication
Analyzing HTTP requests and responses
Using Wireshark display filters
Investigating TCP analysis indicators
Connecting networking theory with real packet traffic
🔍 Useful Wireshark Filters
TCP
tcp
TCP SYN
tcp.flags.syn == 1
TCP Stream
tcp.stream eq 4
DNS
dns
HTTP
http
HTTP Requests
http.request
HTTP Responses
http.response
TCP Retransmissions
tcp.analysis.retransmission
TCP Lost Segments
tcp.analysis.lost_segment
📸 Project Evidence

The repository contains screenshots demonstrating:

TCP three-way handshake
DNS query and response
HTTP GET request
HTTP 200 OK response
TCP analysis findings
⚠️ Disclaimer

This project was performed for educational purposes in a controlled environment using traffic generated from my own system.

No unauthorized systems or networks were targeted.

🚀 Future Improvements

I plan to extend this project by exploring:

TLS/HTTPS packet analysis
Wireshark statistics and graphs
TCP retransmission analysis
Network troubleshooting
Suspicious traffic detection
Basic SOC-style packet investigation
👨‍💻 Skills Demonstrated

Cybersecurity | Network Security | Wireshark | Packet Analysis | TCP/IP | DNS | HTTP | Network Troubleshooting | SOC Fundamentals

⭐ If you found this project useful, feel free to explore the repository.



### 📂 Your GitHub folder should look like this


```text
Wireshark-Network-Traffic-Analysis/
│
├── README.md
│
├── screenshots/
│   ├── 01_TCP_Handshake.png
│   ├── 02_DNS_Analysis.png
│   ├── 03_HTTP_GET.png
│   ├── 04_HTTP_200_OK.png
│   └── 05_TCP_Anomaly.png
│
└── captures/
    └── README.md
