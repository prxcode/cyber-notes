# Networking Fundamentals

### Network
A collection of interconnected devices that can share data. These devices communicate using rules called protocols.

### Types of Network
- **LAN**: Local Area Network
- **WAN**: Wide Area Network
- **MAN**: Metropolitan Area Network
- **PAN**: Personal Area Network

### Network Topologies
- Bus: Single cable, one break = all down
- Star: All connect to central device(like switch)
- Mesh: Devices connect to multiple devices
- Hybrid: Mix of Topologies

### ISP and IP
Internet service provider is the one who provides individuals and organizations access to the internet and other related services (ex. Vodafone). Internet Protocol Address is basically address of that computer, address is required in networking and packet transfer. Every system has IP address (ex 01.234.567.89).
Here, 
- 01 = Country
- 234 = state
- 567 = City/ISP
- 89 = Device ID
IP range between (0-255).

### Variations of IP
- IPv4
    - Address size 32 bit number.
    - Address format dotted decimal(192.159.25.76).
    - Number of address around 4.7 billion address.
- IPv6
    - Address size 128 bit number.
    - Hexadecimal notation(`3ffe:f200:0234:ab00:0123:4567:8901:abcd`).
    - Number of address aound 370 trillion.
 
### Types of IP
- 1. Private IP
  - For LAN(for small network)
  - Private IP !---> Public IP
  - Private IP ---> Private IP(only if both are in same network)
    
- 2. Public IP
  - For WAN(real name for Wider range network)
  - Public IP ---> Public IP(only in WAN network)

- 3. Static IP
  - IP which doesn't change when you reconnect to a network and It remain same forever.
 
- 4. Dynamic IP
  - IP change everytime we reconnect, example when we get disconnected from network our IP is replaced with someone who need.

### MAC Address
Media Access Control Address consist of 48bits = 6byte
Example format `0A:22:84:D5:65:V4`.

To find your MAC Address type 
- Windows: CMD -> `getmac`
- Linux/MacOS -> `ifconfig`
- Or websit -> `https://dnschecker.org/mac-lookup.php`

### Ports(Path/Route)
Ports are basically path from which data is transferred to one IP Address to another. There should be one reciver to recieve packet at that address. Only one person at a time can use that port unless its free. We have 1-65535 Ports

### Types of Ports
- 1. Well known Ports: 0 - 1023 (eg. http/https/dns/ssh/smtp/ftp)
  2. Registered Ports: 1024 - 49151 (eg. mysql servers/rdp)
  3. Dynamic Ports: 49152 - 65535 (eg. private ports/temp use)

### Localhost(127.0.0.1)
It refers to the local commputer itself. It is used for testing web apps, networking without internet access. It runs local servers WAMP or node.js, basically a network which is their in every device for testing and can't be accessed by other devices.

### Allotment of IP
- 1. Manual
    - The IP address is assigned manually by user.
    - It remains fixed unless changed.
    - Configuration is done in device settings.
    - Ex. Servers, Cameras

- 2. Automatic
    - Using DHCP, ARP these protocols help.
    - Most commonly used as faster.
    - Ex. Home/Office wifi
 
  
