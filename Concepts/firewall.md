# Firewall Basics

## What is a Firewall?

A firewall is a security system that monitors and controls incoming and outgoing network traffic based on predefined security rules.

Its primary purpose is to allow legitimate traffic while blocking unauthorized or malicious connections.

---

# Why Firewalls are Important

Firewalls help to:

- Protect systems from unauthorized access.
- Block malicious traffic.
- Reduce the risk of cyber attacks.
- Control network communication.
- Enforce security policies.

---

# Types of Firewalls

## Packet Filtering Firewall

Examines individual packets and allows or blocks them based on rules such as:

- Source IP
- Destination IP
- Protocol
- Port Number

---

## Stateful Firewall

Tracks active network connections.

Instead of checking every packet independently, it determines whether a packet belongs to an existing trusted connection.

---

## Application Firewall

Filters traffic at the application layer.

Example:

- HTTP
- HTTPS
- FTP

It understands application protocols and provides more advanced protection.

---

# Host-based Firewall

Runs on an individual computer.

Examples:

- iptables
- nftables
- UFW
- Windows Defender Firewall

---

# Network Firewall

Protects an entire network by filtering traffic before it reaches internal systems.

Usually installed on:

- Routers
- Dedicated firewall appliances
- Enterprise gateways

---

# Firewall Actions

A firewall rule usually performs one of the following actions:

- ACCEPT → Allow traffic
- DROP → Silently discard traffic
- REJECT → Block traffic and send an error response

---

# Firewall Rules

Firewall rules can filter traffic based on:

- Source IP Address
- Destination IP Address
- Port Number
- Protocol (TCP, UDP, ICMP)
- Network Interface

---

# Common Use Cases

Examples include:

- Allow SSH (Port 22)
- Allow HTTP (Port 80)
- Allow HTTPS (Port 443)
- Block a specific IP address
- Block unused ports

---

# Linux Firewall

Linux commonly uses:

- iptables
- nftables

Many Linux distributions also provide easier management tools such as UFW or FirewallD.

---

# Best Practices

- Allow only required ports.
- Deny unnecessary traffic.
- Keep firewall rules organized.
- Review rules regularly.
- Follow the principle of least privilege.

---

# Summary

A firewall is one of the most important security mechanisms in Linux and networking. It filters network traffic, protects systems from unauthorized access, and enforces security policies using predefined rules.
