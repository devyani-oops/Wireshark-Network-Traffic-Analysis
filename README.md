# Wireshark Network Traffic Analysis

## Task Overview
- Capture live network packets on Kali Linux VM
- Identify basic protocols and traffic types
- Analyze captured data using Wireshark
- **Expert Analysis**: Deep protocol inspection with 200+ warnings and notes

## Capture Session Details
- **Capture Duration**: 46 seconds
- **Total Packets**: 10,866
- **Total Data**: 11 MB
- **Expert Info Items**: 200+ warnings and notes
- **Interface**: eth0

## Protocols Identified & Analyzed
1. **TCP** - 33 connection establishments, 16 terminations
2. **TLS** - 75 deprecated version fields, 5 unknown records
3. **QUIC** - 154 decryption failures, 55 retransmissions
4. **DNS** - 12 missing responses, 2 retransmissions
5. **UDP** - Possible traceroute activity

## Key Findings
- **High TCP Activity**: 33 SYN packets, 16 FIN packets indicating multiple connections
- **QUIC Encryption**: 154 handshake decryption failures (normal for encrypted traffic)
- **TLS Deprecation**: 75 instances of legacy version fields
- **DNS Issues**: 12 missing responses requiring investigation
- **Connection Stability**: Multiple RST packets and retransmissions

## Expert Info Summary
- **Warnings**: 183 items requiring attention
- **Notes**: 107 informational items
- **Chat**: 126 normal protocol operations
