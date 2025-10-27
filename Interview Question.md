# Interview Questions & Answers - Based on Actual Capture

## 1. What is Wireshark used for?
**Answer**: Wireshark is a network protocol analyzer used for network troubleshooting, analysis, and security assessment. In my capture, I used it to analyze 10,866 packets over 46 seconds to understand network traffic patterns.

## 2. What is a packet?
**Answer**: A packet is a formatted unit of data containing headers (control information) and payload (user data). My capture contained 10,866 such packets with an average size of 1039 bytes.

## 3. How to filter packets in Wireshark?
**Answer**: Using display filters like:
- `dns` - Show DNS traffic (observed multiple queries)
- `tcp` - TCP connections (seen in handshakes)
- `http` - HTTP web traffic
- `tls` - Encrypted traffic (observed in my capture)

## 4. Difference between TCP and UDP?
**Answer**: 
- **TCP** (observed): Connection-oriented, reliable, used for web traffic
- **UDP** (used in DNS): Connectionless, faster, used for DNS queries

## 5. What is a DNS query packet?
**Answer**: A DNS query requests domain name resolution. I observed multiple DNS packets converting domain names to IP addresses.

## 6. How can packet capture help in troubleshooting?
**Answer**: From my 11MB capture, I could:
- Verify network connectivity (0% packet loss)
- Identify protocol issues
- Analyze traffic patterns (232 pps)
- Detect security anomalies

## 7. What is a protocol?
**Answer**: A set of rules governing data exchange. My capture showed multiple protocols working together (DNS, TCP, HTTP, TLS).

## 8. Can Wireshark decrypt encrypted traffic?
**Answer**: Only with encryption keys. In my capture, TLS traffic appeared encrypted, but I could analyze the handshake process.
