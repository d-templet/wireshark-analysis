# Wireshark Traffic Analysis Lab

## Project Overview
I captured and analyzed live network traffic on my home network using Wireshark on Fedora Linux. The goal was to identify common protocols, understand how HTTP/TCP work at the packet level, and practice investigative analysis.

## Technologies Used
- **OS:** Fedora Linux
- **Tool:** Wireshark 4.6.4
- **Protocols:** HTTP, TCP, DNS, ARP

## Capture Setup
- **Network:** Home WiFi
- **Interface:** wlp2s0
- **Capture Duration:** ~5 minutes
- **Saved as:** capture.pcapng

---

## Observations

### HTTP Traffic
- Captured HTTP requests to `fedoraproject.org`
- Requests observed:
  - `GET /static/hotspot.txt`
  - `GET /`
- All responses returned `200 OK` (successful)
- Observed **cleartext HTTP** (unencrypted)

### TCP Communication
- Followed a TCP stream (stream eq 7)
- Saw the full HTTP request/response exchange:
  - Request: `GET /static/hotspot.txt HTTP/1.1`
  - Response: `HTTP/1.1 200 OK`
  - Server headers: Apache, Content-Type: text/plain
- Understood that TCP handles the underlying connection

### DNS Queries
- DNS queries preceded the HTTP requests
- Translated `fedoraproject.org` to an IP address
- Normal DNS behavior for web browsing

### ARP Traffic
- ARP requests/responses for local device discovery
- No unusual ARP activity detected

### Suspicious Activity
- No suspicious activity detected
- Traffic appears normal for home network

---

## Screenshots

### Full Capture Overview
![Full Capture](screenshots/capture.png)

### HTTP Filtered Traffic
![HTTP Filter](screenshots/http.png)

### DNS Queries
![DNS Filter](screenshots/dns.png)

### TCP Stream Follow
![TCP Stream](screenshots/tcp.png)

---

## What I Learned

1. **HTTP is cleartext** — I can see the full request and response in Wireshark
2. **TCP streams** — Following a stream shows the complete client-server conversation
3. **Protocol hierarchy** — HTTP, TCP, DNS, and ARP all work together
4. **Filters are powerful** — `http` and `dns` isolate specific traffic instantly
5. **Real-world application** — This is how analysts investigate issues

## Real-World Security Relevance

**What I Noticed:**
- Traffic to `fedoraproject.org` was unencrypted HTTP
- This means: someone on the same network could see the file being downloaded
- This is why HTTPS is important for security

**Why This Matters:**
- Security analysts look for unnecessary HTTP traffic
- Organizations enforce HTTPS everywhere to protect data
- Tools like Wireshark can identify cleartext traffic

## Next Steps
- [x] Capture traffic with Wireshark
- [x] Identify HTTP, DNS, and TCP traffic
- [x] Follow a TCP stream
- [x] Document findings
- [ ] Set up a home lab with multiple devices for more complex captures
- [ ] Create detection rules for suspicious traffic

## Connect With Me
- **Email:** dtemplet578@gmail.com
- **GitHub:** [github.com/d-templet](https://github.com/d-templet)
- **LinkedIn:** [linkedin.com/in/dee-templet-289611360](https://linkedin.com/in/dee-templet-289611360)

---

*Built as part of my journey from CS student to IT professional.*
