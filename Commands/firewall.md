# Firewall (iptables)

This file contains the firewall commands I practiced during the Hack The Box Academy Linux Fundamentals module using **iptables**.

---

# View Firewall Rules

| Command | Description |
|---------|-------------|
| `sudo iptables -L` | List all firewall rules |
| `sudo iptables -L --line-numbers` | List firewall rules with line numbers |

---

# Add Firewall Rules

| Command | Description |
|---------|-------------|
| `sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT` | Allow incoming SSH traffic |
| `sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT` | Allow incoming HTTP traffic |
| `sudo iptables -A INPUT -s IP_ADDRESS -j DROP` | Block traffic from a specific IP address |

---

# Delete Firewall Rules

| Command | Description |
|---------|-------------|
| `sudo iptables -D INPUT RULE_NUMBER` | Delete a rule by its number |

---

# Custom Chains

| Command | Description |
|---------|-------------|
| `sudo iptables -N MYCHAIN` | Create a new custom chain |
| `sudo iptables -A INPUT -j MYCHAIN` | Send INPUT traffic to the custom chain |

---

# Common Chains

| Chain | Purpose |
|-------|---------|
| `INPUT` | Incoming traffic to the local machine |
| `OUTPUT` | Outgoing traffic from the local machine |
| `FORWARD` | Traffic passing through the machine (routing) |

---

# Common Targets

| Target | Description |
|--------|-------------|
| `ACCEPT` | Allow the packet |
| `DROP` | Silently discard the packet |
| `REJECT` | Block the packet and send a rejection response |

---

## Notes

These commands were practiced to understand how Linux firewalls filter network traffic using **iptables**.
