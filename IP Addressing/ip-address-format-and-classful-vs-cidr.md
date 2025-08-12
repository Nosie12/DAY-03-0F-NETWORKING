# IP Address Format and the Shift from Classful to CIDR

## The Structure of an IPv4 Address
- An **IPv4 address** is made up of **32 binary bits**.
- These bits are grouped into **4 sections** called **octets**.
- **One octet = 8 bits = 1 byte**.
- Example formats:
  - **Binary form** – e.g., `11000000.10101000.00000001.00000001`
  - **Dotted decimal notation** – e.g., `192.168.1.1`

Even though we usually see IP addresses in dotted decimal form, **under the hood they are stored and processed as binary numbers**.

---

## Street Analogy – Same House Number, Different Streets
Think of:
- **Street name** = Network portion of the IP address.
- **House number** = Host portion of the IP address.

Rules:
- You **cannot** have two houses with the same number on the same street.
- But **you can** have "House #1" on multiple different streets.
- Similarly:
  - Devices can have the same host number **if** they are on **different networks**.
  - They cannot have the same full IP address on the same network.

---

## From Classful Networking to CIDR
Originally, IPv4 used **Classful Addressing**, which divided IP addresses into five classes (A, B, C, D, E):
- **Class A** – For very large networks (supports ~16 million IP addresses).
- **Class B** – For medium-sized networks (~65,000 IP addresses).
- **Class C** – For small networks (up to 254 IP addresses).
- **Class D** – Reserved for multicast.
- **Class E** – Reserved for experimental use.

**Problems with Classful Addressing:**
- It often wasted large amounts of IP addresses.
- The rigid size categories didn’t fit real-world network needs.

---

## Introduction of CIDR
- In 1993, **Classless Inter-Domain Routing (CIDR)** replaced classful addressing.
- CIDR allows:
  - Flexible division of IP addresses into network and host portions.
  - More efficient use of the address space.
  - Networks of many different sizes, not just the fixed A/B/C sizes.

**Example:**
- A Class A network always had 8 bits for the network and 24 bits for hosts (`/8`).
- CIDR lets you have any number of bits for the network — e.g., `/12`, `/20`, `/29`, etc.

---

## Historical Context
- Classful addressing was fine when the Internet was small.
- As the Internet grew, IP address shortages became a problem.
- CIDR was introduced to conserve addresses and slow down IPv4 exhaustion.
- You may still see some old networking commands (e.g., in legacy routing protocols) using classful notation, but modern networks almost always use CIDR.

---

## Key Takeaways
1. An IPv4 address is **32 bits**, divided into **4 octets**.
2. Network portion = street name; host portion = house number.
3. Classful addressing (A, B, C, D, E) is outdated.
4. CIDR allows more flexible and efficient IP allocation.
5. Some legacy systems still use classful formats, so it’s worth knowing the history.

---
