# OSI Model - 7 Layers 

1. **Physical (Layer 1)**
   - Cables, connectors, signals 
   - Eg: Ethernet cable, fiber optics
2. **Data Link (Layer 2)**
   - Mac address, switches 
   - ARP (resolves IP <-> MAC)
  
3. **Network (Layer 3)**
   - IP addressing, routing 
   - Subnetting device networks 
  
4. **Transport (Layer 4)**
   - TCP, UDP'
   - Use ports 
  
5. **Session (Layer 5)**
   - Manages connection between devices
   - Starts/Stop session

6. **Presentation (Layer 6)**
   - Data format, encryption, compression
  

7. **Application (Layer 7)**
   - Interface for users
   - Eg: Browsers
   - Protocols: HTTP, FTP, SMTP, DNS etc


### HTTP Request
A packet asking to load a website includes GET/POST headers and body. Example of HTTP Request.
- `<request line>` -> GET /doc/test html http/1.1
- `<request header>` -> host/accept/user agent/content length
- `<blank line to seprate header and body>`
- `<request message body>`

#### Types of Request Method
- 1. **GET**: Data transfer through URL easily visible and not secure.
- 2. **POST**: Sends user information & files in body to secure using html forms.
- 3. **PUT**: Replaces all current representations of the target resources with uploaded content.
- 4. **DELETE**: Remove all current representatios of the target resources given by a URL.
- 5. **OPTIONS**: Describe the communication options for the target resource.
- 6. **TRACE**: Performs a message loop back test along the path to the target resource.
- 7. **CONNECT**: Establishes a tunnel to the server identified by given URL.
 
