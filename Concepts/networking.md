# Networking Basics

## What is Networking?

Networking is the process of connecting two or more devices so they can communicate and share data.

Examples:
- Computer to Computer
- Computer to Router
- Computer to Server
- Mobile to Wi-Fi

---

# Why Networking is Important?

Networking allows systems to:

- Share files
- Access the Internet
- Connect to remote systems
- Host websites
- Communicate securely

---

# IP Address

An IP Address is a unique identifier assigned to every device on a network.

Example:

192.168.1.10

Types:

- Private IP
- Public IP

---

# Subnet Mask

A subnet mask separates the network portion from the host portion of an IP address.

Example:

255.255.255.0

---

# Default Gateway

The default gateway is the router that forwards traffic outside the local network.

Without a gateway, a device can only communicate within its own network.

---

# DNS (Domain Name System)

DNS translates domain names into IP addresses.

Example:

google.com
↓

142.x.x.x

Common DNS Servers:

- 8.8.8.8 (Google)
- 1.1.1.1 (Cloudflare)

---

# MAC Address

A MAC Address is the physical address of a network interface.

Characteristics:

- Assigned by the manufacturer
- Unique for each network card
- Used for communication inside a local network

---

# Ports

Ports identify specific network services.

Common Ports:

| Port | Service |
|------|---------|
| 22 | SSH |
| 21 | FTP |
| 80 | HTTP |
| 443 | HTTPS |
| 2049 | NFS |
| 3306 | MySQL |

---

# Common Networking Protocols

## HTTP
Transfers web pages.

## HTTPS
Secure version of HTTP using encryption.

## SSH
Provides secure remote login.

## FTP
Transfers files between systems.

## NFS
Allows sharing folders across Linux systems.

---

# Network Troubleshooting

Common tools:

- ping
- traceroute
- ip
- netstat
- ss

These tools help verify connectivity, routing, interfaces, and listening ports.

---

# Packet Flow

A typical network communication follows this path:

Application
↓

Transport Layer (TCP/UDP)
↓

IP Layer
↓

Network Interface
↓

Router
↓

Internet
↓

Destination Server

---

# Key Concepts

- Every device needs an IP address.
- DNS converts domain names into IP addresses.
- Routers connect different networks.
- Switches connect devices within the same network.
- Firewalls control incoming and outgoing traffic.
- Ports identify specific network services.

---

# Summary

Networking enables communication between devices using IP addresses, protocols, routers, switches, DNS, and ports. Understanding these concepts is essential before learning firewalls, SSH, web servers, and network security.
