# IP Addressing and IP Protocol Basics – Beginner Friendly

## DNS and IP Address Resolution
Every website you visit has an IP address, but people remember names better than numbers.  
**DNS** (Domain Name System) acts like the internet’s phonebook:
- You type a name like `cnn.com` or `google.com`.
- DNS finds the matching IP address for that name.
- This lets your computer connect to the correct server.

You can test this by "pinging" a website or by using tools that only perform DNS lookups (without sending extra traffic to the site). Different sites will resolve to different IP addresses, even for big names.

---

## Every Device Has an IP Address
- Your own computer or phone also has its own IP address.
- On Windows, you can see it with the command `ipconfig`.
- Devices can have:
  - **IPv4 addresses** (the older format, dotted decimal like `192.168.1.1`)
  - **IPv6 addresses** (a newer format, uses hexadecimal, created because IPv4 addresses are running out).

---

## The Role of IP in Networking
IP (Internet Protocol) is part of the **network layer** in the OSI model.
- IP is **connectionless** – it does not set up a formal session before sending data.
- Each packet is treated separately and can take different routes to the destination.
- This is different from **TCP**, which is connection-oriented and requires a “three-way handshake” before sending data.

---

## Connectionless vs. Connection-Oriented
- **Connectionless (IP, UDP)**:  
  No handshake, no guarantee of delivery, no tracking of lost or corrupted packets.  
  Each packet is sent on its own, without confirmation from the receiver.
  
- **Connection-Oriented (TCP)**:  
  Uses a handshake to establish a session, ensures packets are delivered in order, and retransmits lost ones.

---

## Routing with IP
Routers decide where to send packets based on the **network portion** of the IP address, not the host portion.  
Different routing protocols use different methods:
- **RIP**: Chooses routes based on hop count (older, less efficient).
- **OSPF**: Chooses routes based on bandwidth.
- Others: Use different metrics to find the “best path.”

Because IP treats each packet individually, packets from the same communication can travel along different routes to reach the same destination.

---

## Reliability and Limitations of IP
- IP only makes a **“best effort”** to deliver packets.
- Packets can be:
  - Lost
  - Delayed
  - Duplicated
  - Sent out of order
- Recovery, retransmission, and error checking are handled by higher-level protocols like TCP, not IP itself.

---

## IPv4 Address Format
- An IPv4 address is **32 bits** long.
- It’s written as four **octets** (8 bits each) in dotted decimal format (e.g., `192.168.10.5`).
- Each octet can range from **0 to 255**.
- The address is split into:
  - **Network portion** – identifies the network
  - **Host portion** – identifies the specific device within that network

---

## IP Addressing and Delivery Analogy
Think of IP addresses like a package delivery service:
- **Network portion** = City or postal code
- **Host portion** = Street address or apartment number
- Routers use the **network portion** to decide the general route.
- Within the network, the host portion is used to deliver to the exact device.

---
