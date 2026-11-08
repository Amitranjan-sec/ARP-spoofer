# Python ARP Spoofer & Network Traffic Restorer

A command-line tool built with Python and **Scapy** to perform ARP spoofing (Man-in-the-Middle) and gracefully restore original network routing in a lab environment.

---

## 🛠️ How It Works

This script leverages the Address Resolution Protocol (ARP) to manipulate the ARP caches of a target device and a gateway (access point):
1. **ARP Spoofing:** Sends forged ARP response packets to the victim claiming to be the router, and to the router claiming to be the victim[cite: 2, 8, 9]. This intercepts traffic flow through the hacker's machine[cite: 2].
2. **Exception Handling:** Uses `try/except` blocks to catch keyboard interrupts (`Ctrl+C`)[cite: 11, 12].
3. **Traffic Restoration:** Automatically broadcasts correct ARP packets before exiting to restore normal network routing and prevent connection drops[cite: 8, 9].

---

## 📋 Prerequisites & Requirements

* **OS:** Kali Linux (or any Linux distribution with network tool support)
* **Python:** Python 3.x
* **Library:** Scapy

Install dependencies via pip:
```bash
pip install -r requirements.txt
