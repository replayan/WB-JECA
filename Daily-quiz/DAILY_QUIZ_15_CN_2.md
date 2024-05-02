# Computer Networks QUIZ

Date: May 02, 2024

**Source:** [Jecacracker](https://jecacracker.in/Daily_Quiz/)

---

1. **IP is responsible for ______ communication while TCP is responsible for ______ communication.**

   - **a) host-to-host; process-to-process**
    - b) process-to-process; host-to-host
    - c) process-to-process; process-to-process
    - d) node-to-node; host-to-host

   *Explanation:*  
   IP (Internet Protocol) operates at the network layer of the OSI model and is responsible for logical addressing and routing of data packets between hosts on a network. TCP (Transmission Control Protocol) operates at the transport layer of the OSI model and is responsible for establishing and maintaining reliable end-to-end communication between applications running on different hosts.

2. **In the computer network, Open Systems Interconnection model has seven layers within which ______ layer is used for routing.**

   - a) application
   - **b) network**
   - c) session
   - d) transport

   *Explanation:*  
   The seven layers of the OSI model are:
   1. Physical layer
   2. Data Link layer
   3. Network layer (used for routing)
   4. Transport layer
   5. Session layer
   6. Presentation layer
   7. Application layer

   The network layer is responsible for logical addressing, routing, and forwarding of data packets between networks.

3. **The physical layer is responsible for _____.**

   - a) line coding
   - b) channel coding
   - c) modulation
   - **d) all of the mentioned**

   *Explanation:*  
   The physical layer is responsible for the actual transmission of data over the physical medium. Its functions include:
   - Line coding: Converting digital data into appropriate signals for transmission
   - Channel coding: Adding redundant bits for error detection and correction
   - Modulation: Encoding digital data into analog signals for transmission

4. **Maximum number of host addresses that is possible for a network with a subnet mask 255.255.240.0 is _______.**

   - a) 256
   - b) 1024
   - **c) 4094**
   - d) 4096

   *Explanation:*  
   - The subnet mask 255.255.240.0 has 20 bits set to 1, which means the network portion is 20 bits long.
   - The remaining 12 bits are available for host addressing.
   - With 12 bits, the maximum number of host addresses is 2^12 - 2 = 4094 (two addresses are reserved for network and broadcast addresses).

5. **What are the Methods to move data through a network of links and switches?**

   - a) Packet switching and Line switching
   - b) Circuit switching and Line switching
   - c) Line switching and bit switching
   - **d) Packet switching and Circuit switching**

   *Explanation:*  
   - Packet switching: Data is divided into small packets, which are transmitted independently over the network. Packets may take different paths and are reassembled at the destination.
   - Circuit switching: A dedicated end-to-end connection is established between the source and destination before data transmission begins. The connection is maintained for the entire duration of the communication.

   Line switching and bit switching are not common methods used in modern networks.
