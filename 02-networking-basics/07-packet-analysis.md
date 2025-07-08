# Packet Analysis Basics

### What is a Packet?
A packet is a small unit of data transmitted across a network, containing:

- Header: Info like source/destination IP, port, protocol
- Payload: Actual data

### TCP Handshake:
- SYN: Client sends request to server
- SYN-ACK: Server acknowledges
- ACK: Client finalizes connection

### Packet Capture with Wireshark:
- Wireshark: Tool for monitoring network packets
- Can view: IP addresses, protocols, flags (e.g., SYN, ACK), payloads