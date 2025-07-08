#  IP Addressing & Subnetting

### IPv4 vs IPv6:
- **IPv4**: 32-bit, e.g., 192.168.0.1, ~4.3 billion addresses
- **IPv6**: 128-bit, e.g., 2001:0db8:85a3::8a2e:0370:7334, much larger space

### Private IPs
Used inside LAN, not routable on Internet

- IPv4 ranges:
    - 10.0.0.0 – 10.255.255.255
    - 172.16.0.0 – 172.31.255.255
    - 192.168.0.0 – 192.168.255.255

### Public IPs
Unique and routable on Internet.

### Subnet Mask
Defines which portion of IP is network and which is host.
Example:
255.255.255.0 → /24 in CIDR notation