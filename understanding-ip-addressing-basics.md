# Understanding IP Addressing – A Beginner-Friendly Guide

An **IP address** (Internet Protocol address) is a unique logical address given to a device on a network so it can communicate with other devices. It works like a street address for your home: every house has a unique address so mail gets to the right place, and every device needs a unique IP address so data knows where to go.

---

## IP Addresses vs. MAC Addresses

- **MAC Address**: A permanent, physical address built into your network card by the manufacturer. Think of it like your device’s fingerprint—it doesn’t change.
- **IP Address**: A logical address assigned by an administrator or automatically by a service like **DHCP** (Dynamic Host Configuration Protocol). IP addresses can change, especially when you reconnect to a network.

---

## Why IP Addresses Are Important

- Every device on the internet must have a **unique public IP address** to communicate.
- If two devices had the same public IP at the same time, it would cause a conflict and break communication.
- Inside private networks (like your home Wi-Fi), devices can use **private IP addresses**, but these must be translated to a **public IP** when connecting to the internet. This translation is done by **NAT** (Network Address Translation).

---

## Public vs. Private IP Addresses

- **Private IP addresses** are used inside local networks and are not visible directly on the internet.
- **Public IP addresses** are globally unique and used for communication across the internet.
- Example: Many organizations use private IPs internally, and their router translates these into a public IP when sending data outside.

---

## IP Address Versions

There are two main versions in use:
1. **IPv4** – The older version, written as four numbers separated by dots (e.g., `192.168.1.1`).
2. **IPv6** – The newer version, created because IPv4 addresses are running out. IPv6 uses a longer, hexadecimal format.

---

## Classes of IPv4 Addresses

IPv4 addresses are grouped into classes based on their first octet (the first number before the first dot):
- **Class A**: Large networks (first octet: 1–126)
- **Class B**: Medium-sized networks (first octet: 128–191)
- **Class C**: Small networks (first octet: 192–223)
- **Class D**: Special use for multicast
- **Class E**: Reserved for experimental use

---

## Special IPv4 Addresses

Some IPv4 addresses have special purposes:
- **Loopback (127.0.0.1)** – Refers to the device itself (“localhost”).
- **Broadcast address** – Sends data to all devices on a network.
- **Private address ranges** – Not routable on the internet; used inside local networks.

---

## DNS – Turning Names into IPs

Humans remember names better than numbers. **DNS** (Domain Name System) works like an internet phonebook:
- You type a website name like `yahoo.com`.
- DNS translates it into an IP address (e.g., `74.6.231.21`).
- Your computer uses that IP address to connect to the website’s server.

---

## Example of IP Resolution

1. You type `yahoo.com` in your browser.
2. DNS finds its IP address.
3. Your device connects directly to that IP.
4. Some websites block certain tests like **ping**, but the DNS lookup still works.

---

## Subnet Masks

A **subnet mask** defines which part of the IP address refers to the network and which part refers to the device (host).  
Routers use this to determine if the destination is inside the same network or needs to be sent elsewhere.

---

## Key Takeaways

- IP addresses uniquely identify devices in a network.
- Private IPs are for local use; public IPs are for internet communication.
- IPv4 addresses are running out, so IPv6 is being used more.
- DNS makes the internet easier by translating names into IP addresses.
- Subnet masks and address classes help organize and manage networks.

---
