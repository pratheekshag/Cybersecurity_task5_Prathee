# Cybersecurity_task5_Prathee
Capture and Analyze Network Traffic Using Wireshark.

---

## Steps Performed

1. **Installed Wireshark**
   - Downloaded from the [official website](https://www.wireshark.org/download.html).
   - Installed with **Npcap** support for live packet capturing.

2. **Started Packet Capture**
   - Opened Wireshark and selected the **active network interface** (Wi-Fi).
   - Clicked the blue **Start Capturing Packets** icon.

3. **Generated Network Traffic**
   - Opened a web browser and visited multiple websites (e.g., `openai.com`, `example.com`).
   - Also executed a ping command in Command Prompt:
     ping 8.8.8.8
   - This generated HTTP, DNS, and ICMP packets.

4. **Stopped Capture**
   - After about one minute, clicked the **red square (🟥)** icon to stop capturing.

5. **Filtered Packets by Protocol**
   - Used Wireshark display filters:
     - `http` → For web traffic  
     - `dns` → For domain resolution  
     - `tcp` → For connection management  
     - `icmp` → For ping requests/replies

6. **Identified Protocols**
   - At least three different protocols were identified: **DNS**, **TCP**, **HTTP**, and **ICMP**.

7. **Exported Capture File**
   - Saved the capture as `network_capture.pcap` in the **Downloads** folder.

---

## 📊 Findings and Analysis

| **Protocol** | **Function** | **Observation** |
|---------------|---------------|----------------|
| **DNS** | Resolves domain names to IP addresses. | Observed queries to resolve domains such as `openai.com` and `example.com`. |
| **TCP** | Ensures reliable delivery of packets between client and server. | Multiple TCP handshakes (SYN, SYN-ACK, ACK) seen for web connections. |
| **HTTP** | Used for web communication. | GET and response packets captured during website browsing. |
| **ICMP** | Used for testing connectivity. | Echo request and reply packets observed for `ping 8.8.8.8`. |

### **General Statistics**
- Duration: ~1 minute  
- Total packets captured: ~3,000 (approximate)  
- Average packet size: 100–200 bytes  
- Source IP: Local machine IP (e.g., `192.168.x.x`)  
- Destination IPs: DNS resolver (8.8.8.8) and visited websites  

### **Analysis Summary**
The capture reflects typical user internet activity:
- DNS lookups occur before HTTP requests.
- TCP connections are established to manage reliable delivery.
- HTTP traffic shows data exchange with websites.
- ICMP confirms basic network connectivity.

---

## 🧾 Conclusion
This exercise successfully demonstrated the process of capturing and analyzing live network traffic using Wireshark.  
Multiple protocols were identified and studied, showing how different layers of the OSI model interact in real-time network communication.
