# Wireshark Expert Information Analysis

## Executive Summary
The capture contains 10,866 packets with 416 Expert Info items across three severity levels, revealing both normal operations and potential network issues.

## Detailed Protocol Analysis

### TCP Protocol (88 Events)
**Connection Management:**
- 35 SYN packets (connection requests)
- 33 SYN+ACK packets (connection acknowledgments)
- 16 FIN packets (connection terminations)
- 8 connection initiation/closing frames

**Sequence Issues:**
- 3 previous segments not captured (common at start)
- 2 ACKed segments not captured
- 9 suspected retransmissions
- 5 duplicate ACKs
- 3 D-SACK sequences (Duplicate Selective Acknowledgement)

**Connection Problems:**
- 2 Connection reset (RST) packets
- 7 TCP keep-alive segments
- 7 ACKs to keep-alive segments

### TLS Protocol (80 Events)
**Security Observations:**
- 75 deprecated version fields (TLS legacy versions)
- 5 ignored unknown records
- **Impact**: Mixed TLS versions indicating varied client support

### QUIC Protocol (222 Events)
**Encryption Challenges:**
- 154 failed handshake decryptions (expected for encrypted QUIC)
- 55 reused stream offsets (possible retransmissions)
- 13 coalesced padding data frames

### DNS Protocol (14 Events)
**Resolution Issues:**
- 12 missing DNS responses
- 1 DNS response retransmission
- 1 DNS query retransmission
- **Impact**: Potential DNS server problems or packet loss

### UDP Protocol
- 2 possible traceroute packets detected

## Severity Breakdown

###  Warnings (183 items)
**Critical Issues:**
- Connection resets indicate abrupt terminations
- Missing DNS responses affect name resolution
- Failed QUIC decryption (normal for security)

**Moderate Issues:**
- Sequence number gaps at capture start
- TLS unknown records

###  Notes (107 items)
**Informational:**
- Normal connection lifecycle (SYN, FIN)
- Keep-alive mechanisms
- Retransmission patterns

###  Chat (126 items)
**Normal Operations:**
- Standard connection establishment
- Protocol version negotiations
- Expected protocol behaviors

## Network Health Assessment

###  Normal Behaviors
- TCP three-way handshakes completed
- Connection clean terminations (FIN)
- QUIC encryption working as expected
- Mixed TLS versions (common in heterogeneous networks)

###  Areas for Investigation
1. **DNS Reliability**: 12 missing responses suggest DNS server issues
2. **Connection Stability**: RST packets indicate potential

### RESULTS
![image alt](https://github.com/devyani-oops/Wireshark-Network-Traffic-Analysis/blob/d78881375edbf66ada2054080c8516e0f9609fe0/Screenshot%202025-10-27%20120420.png)
![image alt](https://github.com/devyani-oops/Wireshark-Network-Traffic-Analysis/blob/bbf69ae364364f53317ce89cddbb990978af8769/Screenshot%202025-10-27%20120450.png)
![image alt](https://github.com/devyani-oops/Wireshark-Network-Traffic-Analysis/blob/fb33bde08504e3fe0e03d6011b791d67741af513/Screenshot%202025-10-27%20120515.png)
![image alt](https://github.com/devyani-oops/Wireshark-Network-Traffic-Analysis/blob/b9adf2ce0ba80f30990a50ce2ec9c72c9680a8fa/Screenshot%202025-10-27%20120723.png)

