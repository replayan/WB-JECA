# Computer Network

## 1. Concepts of Networking
- **Definition**: A computer network is a collection of interconnected devices that can communicate with each other to share resources and information.
- **Purpose**: Facilitates data exchange and resource sharing between multiple devices, enabling collaboration and communication.
- **Components**: Nodes (computers, servers, routers), Communication links (wired, wireless), Networking devices (switches, hubs, modems).

---

## 2. Application Areas
- **Business Applications**: Facilitates communication within organizations, sharing of files, and collaborative work.
- **Internet**: Enables global communication, access to information, and online services.
- **Home Networking**: Connects devices within a household for sharing resources like printers and internet access.
- **Education and Research**: Supports distance learning, collaborative research, and access to online libraries and resources.

---

## 3. Classification
- **Based on Scale**: LAN (Local Area Network), WAN (Wide Area Network), MAN (Metropolitan Area Network).
- **Based on Connection**: Peer-to-Peer, Client-Server.
- **Based on Topology**: Bus, Star, Ring, Mesh.

---

## 4. Reference Models: OSI Model & TCP/IP Model

- The OSI (Open Systems Interconnection) model is a conceptual framework that standardizes the functions of a telecommunication or computing system into seven distinct layers. Each layer serves a specific purpose in facilitating communication between devices over a network.
- The TCP/IP (Transmission Control Protocol/Internet Protocol) model is a concise framework that was developed prior to the OSI model and is the foundation of the modern internet.

### 1. Physical Layer
- **Purpose**: Responsible for transmitting raw data bits over a physical medium.
- **Functions**: Encoding, signaling, and modulation.
- **Example**: Ethernet cables, optical fibers, wireless transmission.

### 2. Data Link Layer
- **Purpose**: Provides error detection and correction within the physical layer.
- **Functions**: Framing, error detection, flow control.
- **Example**: Ethernet switches, Wi-Fi access points.

### 3. Network Layer
- **Purpose**: Handles packet routing, addressing, and forwarding.
- **Functions**: Logical addressing (IP addresses), routing (determining the best path), fragmentation, and reassembly.
- **Example**: Routers, IP protocol.

### 4. Transport Layer
- **Purpose**: Ensures end-to-end communication reliability and data integrity.
- **Functions**: Segmentation, reassembly, flow control, error recovery.
- **Example**: TCP (Transmission Control Protocol), UDP (User Datagram Protocol).

### 5. Session Layer
- **Purpose**: Establishes, manages, and terminates connections between applications.
- **Functions**: Session establishment, synchronization, maintenance, and termination.
- **Example**: Session initiation protocols (SIP), remote procedure call (RPC).

### 6. Presentation Layer
- **Purpose**: Handles data translation, encryption, and decryption.
- **Functions**: Data compression, encryption, decryption, and data formatting.
- **Example**: SSL/TLS, ASCII, JPEG, GIF.

### 7. Application Layer
- **Purpose**: Provides network services directly to end-users and applications.
- **Functions**: Interface between the application and the network, provides services like email, file transfer, and web browsing.
- **Example**: HTTP, FTP, SMTP, DNS.

### Comparison

| **Aspect**              | **OSI Model**                                                  | **TCP/IP Model**                                               |
|-------------------------|----------------------------------------------------------------|----------------------------------------------------------------|
| **Layers**              | Consists of seven layers.                                      | Consists of four layers.                                       |
| **Conceptual vs. Real** | Conceptual model, not implemented in real networks.             | Practical model, directly implemented in the internet protocol suite. |
| **Layering**            | Each layer performs a specific set of functions.                | Overlaps and combines functions across layers for efficiency.   |
| **Complexity**          | More complex due to the number of layers.                      | Simpler due to fewer layers.                                   |
| **Adoption**            | Not directly implemented in networking protocols.               | Used as the basis for the internet protocol suite.             |
| **Flexibility**         | Provides a structured approach to networking.                  | Allows for more flexibility and adaptation to different network environments. |
| **Standardization**     | OSI standards were developed by the ISO (International Organization for Standardization). | TCP/IP standards were developed by the IETF (Internet Engineering Task Force). |
| **Examples**            | OSI model is a theoretical concept.                             | TCP/IP model is the basis for the internet and is widely implemented in networking protocols. |

### Differences in Layers

**1. Comparison in Layers**:

- **Physical Layer**: Both models include a physical layer for transmitting raw data bits over a physical medium.
- **Data Link Layer**: Both models have similar functions for error detection and correction within the physical layer.
- **Network Layer**: Equivalent to the Internet Layer in the TCP/IP model, responsible for routing and addressing.
- **Transport Layer**: Functions similarly in both models, ensuring end-to-end communication reliability and data integrity.
- **Session, Presentation, and Application Layers**: The OSI model separates these layers, while the TCP/IP model combines their functions into the Application Layer.

**2. TCP/IP Model's Advantages**:

- **Simplicity**: The TCP/IP model is simpler with fewer layers, making it easier to implement and understand.
- **Direct Implementation**: The TCP/IP model is directly implemented in the internet protocol suite, providing a practical framework for networking.

**3. OSI Model's Advantages**:

- **Layered Approach**: The OSI model provides a structured approach to networking, allowing for more granular control and abstraction of functions.

**Example Scenario**:
Consider the scenario of sending a webpage request from a browser to a web server:

1. **Application Layer (OSI)** / **Application Layer (TCP/IP)**: The browser interacts with the web server using HTTP (Hypertext Transfer Protocol).
2. **Transport Layer (OSI)** / **Transport Layer (TCP/IP)**: TCP ensures reliable delivery of web page data.
3. **Internet Layer (OSI)** / **Internet Layer (TCP/IP)**: IP handles routing and addressing to ensure the webpage request reaches its destination.
4. **Network Interface Layer (OSI)** / **Link Layer (TCP/IP)**: Handles transmission of data over the physical medium, such as Ethernet or Wi-Fi.

**Example Scenario**:
Consider the scenario of sending an email from one computer to another:

1. **Application Layer**: The email application (e.g., Outlook, Gmail) interacts with the email server using SMTP (Simple Mail Transfer Protocol).
2. **Presentation Layer**: The message is formatted into a standardized email format, and attachments may be encoded.
3. **Session Layer**: A session is established between the client and the server to exchange email data.
4. **Transport Layer**: TCP (or sometimes UDP) ensures reliable delivery of email packets.
5. **Network Layer**: IP handles routing and addressing to ensure the email reaches its destination.
6. **Data Link Layer**: Ethernet or Wi-Fi protocols provide error detection and correction as the email data is transmitted over the physical medium.
7. **Physical Layer**: Raw bits of email data are transmitted over cables or wireless signals.

---

## 5. Transmission Environment & Technologies
- **Medium**: Wired (Twisted Pair, Coaxial Cable, Fiber Optics) and Wireless (Radio Waves, Microwave, Infrared).
- **Technologies**: Ethernet, Wi-Fi, Bluetooth, 3G/4G/5G Cellular, Satellite.

---

## 6. Routing Algorithms
- **Definition**: Determines the path data packets should take from source to destination in a network.
- **Types**: Distance Vector (e.g., RIP), Link State (e.g., OSPF), Path Vector (e.g., BGP).

---

## 7. IP, UDP & TCP Protocols
- **IP (Internet Protocol)**: Provides addressing and routing for data packets.
- **UDP (User Datagram Protocol)**: Connectionless protocol for sending datagrams without guaranteed delivery.
- **TCP (Transmission Control Protocol)**: Connection-oriented protocol for reliable and ordered delivery of data.

---

## 8. IPv4 and IPv6
- **IPv4**: 32-bit address space, represented in dotted-decimal notation (e.g., 192.168.1.1).
- **IPv6**: 128-bit address space, represented in hexadecimal notation (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334).

---

## 9. Reliable Data Transferring Methods
- **Acknowledgment**: Receiver sends acknowledgment for received data packets.
- **Sequence Numbers**: Ensures ordered delivery of packets.
- **Retransmission**: Resends lost or corrupted packets.

---

## 10. Application Protocols
- **HTTP (Hypertext Transfer Protocol)**: For transferring hypertext documents on the World Wide Web.
- **FTP (File Transfer Protocol)**: For transferring files between a client and a server.
- **SMTP (Simple Mail Transfer Protocol)**: For sending email messages.

---

## 11. Network Security
- **Firewalls**: Filter network traffic to prevent unauthorized access.
- **Encryption**: Protects data from being intercepted by encrypting it.
- **Authentication**: Verifies the identity of users and devices accessing the network.

---

## 12. Management Systems
- **SNMP (Simple Network Management Protocol)**: Standard protocol for managing and monitoring network devices.
- **Syslog**: Standard for logging program messages and system events.

---

## 13. Perspectives of Communication Networks
- **Technical Perspective**: Focuses on the hardware and software components of the network.
- **Social Perspective**: Considers the impact of networks on society, culture, and communication patterns.
- **Economic Perspective**: Analyzes the costs and benefits of network deployment and usage.
