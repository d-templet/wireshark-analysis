# Wireshark Traffic Analysis Lab

## Project Overview
I captured and analyzed live network traffic on my home network using Wireshark on Fedora Linux. The goal was to identify common protocols, unusual traffic patterns, and practice investigative analysis.

## Technologies Used
- **OS:** Fedora Linux
- **Tool:** Wireshark
- **Protocols:** HTTP, DNS, TCP, UDP, ICMP

## Capture Setup
- **Network:** Home WiFi
- **Interface:** wlan0
- **Capture Duration:** ~5 minutes
## Screenshots

### Full Capture
![Full Capture](screenshots/full-capture.png)

### HTTP Filtered Traffic
![HTTP Filter](screenshots/http-filter.png)

### DNS Queries
![DNS Filter](screenshots/dns-filter.png)

### TCP Stream Follow
![TCP Stream](screenshots/tcp-stream.png)

## Observations
- HTTP traffic detected (cleartext requests)
- DNS queries for common domains
- Normal ARP traffic for local network discovery

## What I Learned
- How to filter by protocol (`http`, `dns`, `tcp.port==80`)
- How to follow TCP streams
- The difference between encrypted and unencrypted traffic

## Connect With Me
- **Email:** dtemplet578@gmail.com
- **GitHub:** [github.com/d-templet](https://github.com/d-templet)
- **LinkedIn:** [linkedin.com/in/dee-templet-289611360](https://linkedin.com/in/dee-templet-289611360)
