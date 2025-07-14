# Protocols
Set of rules that define how data is transmitted between devices. (eg. http/https/txp/ip/ssh/dns/ftp)

### Types of Protocols in other words TCP/IP model(framework) 

> OSI is a theoretical model, TCP/IP is used in real-world networking. Basically TCP/IP model is a version of OSI model 

A simple table for OSI model with 4 layers
| TCP/IP Layer       | OSI Equivalent | Protocols            |                  Protocols                  |
| ------------------ | -------------- | -------------------- | ------------------------------------------- |
| **Application**    | Layers 5–7     | HTTP, FTP, DNS, SMTP |  This is where high level protocols operate |
| **Transport**      | Layer 4        | TCP, UDP             |  This layer is responsible for end-end communication and error recovery |
| **Internet**       | Layer 3        | IP, ICMP             |  This layer handles the routing of data across the network |
| **Network Interface** | Layers 1–2     | Ethernet, Wi-Fi      |  This layer deals with the physical transmission of data over the network  |

> Most important protocols are TCP and UDP

### How TCP works 
- URG(urgent): Data contained in the packet should be processed immediately
- FIN(finish): There will be no further transmission
- RST(reset): Resets a connection
- PSH(push): Sends all buffered data immediately
- ACK(acknowledgment): Acknowledgment the reciept of a packet
- SYN(synchronize): Initiates a conection between hosts

### TCP has 3 way handshake
- SYN
- SYN, ACK
- ACK

### TCP session termination
- FIN
- ACK
- FIN
- ACK

| TCP(Transmission Control Protocol)  |   UDP (User Datagram Protocol)  | 
| ----------------------------------- | -------------- |
| Handshake and acknowledgment                  | Request, response    |
| Slow        | fast    |
| More reliable, used for web browsing, email and file transfer                        | unsafe and less reliable, used for livestream, VoIP       |

