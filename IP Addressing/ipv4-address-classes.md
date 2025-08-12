# Understanding IPv4 Address Classes (A, B, C, D, E)

IPv4 addresses are grouped into different classes based on the **first octet** (the first 8 bits).  
Each class has a specific range and purpose, and a way to split the address into **network** and **host** portions.

---

## 📌 Class A Addresses

**How to identify:**
- First bit in binary is always `0`.
- Example in binary: `0xxxxxxx`
- Decimal range in first octet: **1 to 126**

**Range:**
- `1.0.0.0` → `126.255.255.255`
- `0.x.x.x` is reserved for the default network and **cannot** be used.
- `127.x.x.x` is reserved for **loopback** (localhost/testing) and **cannot** be assigned to devices.

**Network/Host split:**
- First 8 bits (1 octet) → Network portion
- Remaining 24 bits (3 octets) → Host portion

**Example:**
- IP: `10.0.0.1`  
- Network: `10`  
- Host: `0.0.1`

---

## 📌 Class B Addresses

**How to identify:**
- First two bits in binary: `10`
- Example in binary: `10xxxxxx`
- Decimal range in first octet: **128 to 191**

**Range:**
- `128.0.0.0` → `191.255.255.255`

**Network/Host split:**
- First 16 bits (2 octets) → Network portion
- Remaining 16 bits (2 octets) → Host portion

**Example:**
- IP: `172.16.5.9`  
- Network: `172.16`  
- Host: `5.9`

---

## 📌 Class C Addresses

**How to identify:**
- First three bits in binary: `110`
- Example in binary: `110xxxxx`
- Decimal range in first octet: **192 to 223**

**Range:**
- `192.0.0.0` → `223.255.255.255`

**Network/Host split:**
- First 24 bits (3 octets) → Network portion
- Last 8 bits (1 octet) → Host portion

**Example:**
- IP: `192.168.1.1`  
- Network: `192.168.1`  
- Host: `1`

---

## 📌 Class D Addresses (Multicast)

**How to identify:**
- First four bits in binary: `1110`
- Example in binary: `1110xxxx`
- Decimal range in first octet: **224 to 239**

**Usage:**
- Used for **multicast** — one sender sends data to multiple receivers.

**Examples:**
- `224.0.0.5` — OSPF multicast address  
- `224.0.0.6` — OSPF DR/BDR communication  
- The range `224.0.0.x` is **link-local multicast** — does not leave local network.

---

## 📌 Class E Addresses (Experimental/Research)

**How to identify:**
- First four bits in binary: `1111`
- Example in binary: `1111xxxx`
- Decimal range in first octet: **240 to 255**

**Usage:**
- Reserved for **experimental or future use**.
- Generally **not used** for normal device addressing.
- Includes the broadcast address `255.255.255.255`.

---

## 📝 Important Notes

- **CIDR (Classless Inter-Domain Routing)** has replaced classful addressing in modern networks.  
- However, understanding classes helps in legacy systems and networking basics.  
- Two devices can have the **same host portion** if they belong to **different networks**.  
- Reserved IPs:
  - `127.x.x.x` — loopback addresses (localhost).
  - `0.x.x.x` — default network (invalid for hosts).
  - `255.255.255.255` — broadcast address.

---

## Summary Table

| Class  | First Octet Range | Binary Prefix | Network Bits | Host Bits | Usage                  |
|--------|-------------------|---------------|--------------|-----------|------------------------|
| A      | 1 – 126           | 0xxxxxxx      | 8            | 24        | Large networks         |
| B      | 128 – 191         | 10xxxxxx      | 16           | 16        | Medium networks        |
| C      | 192 – 223         | 110xxxxx      | 24           | 8         | Small networks         |
| D      | 224 – 239         | 1110xxxx      | N/A          | N/A       | Multicast addresses    |
| E      | 240 – 255         | 1111xxxx      | N/A          | N/A       | Experimental use       |

---

Feel free to ask if you'd like me to generate visual diagrams or subnetting examples too!
