# 03 - Firewall Lab

## Objective
Learn how to configure firewall rules, manage network access, and use AppArmor for application security.

---

## Lab 1 - View Existing Firewall Rules

### Command

```bash
sudo iptables -L
```

### Tasks

- View all current firewall rules.
- Identify the INPUT, OUTPUT, and FORWARD chains.

---

## Lab 2 - Allow Traffic on a Specific Port

### Command

```bash
sudo iptables -A INPUT -p tcp --dport 22 -j ACCEPT
```

### Tasks

- Allow incoming SSH traffic.
- Verify the rule has been added.

---

## Lab 3 - Block a Specific IP Address

### Command

```bash
sudo iptables -A INPUT -s 192.168.1.100 -j DROP
```

### Tasks

- Block all traffic from a specific IP.
- Confirm the rule using `iptables -L`.

---

## Lab 4 - Delete a Firewall Rule

### Commands

```bash
sudo iptables -L --line-numbers
sudo iptables -D INPUT 1
```

### Tasks

- Display rule numbers.
- Delete a selected firewall rule.

---

## Lab 5 - Create a Custom Chain

### Commands

```bash
sudo iptables -N MYCHAIN
sudo iptables -A INPUT -j MYCHAIN
```

### Tasks

- Create a custom firewall chain.
- Redirect incoming traffic to the custom chain.

---

## Lab 6 - Restrict SSH Access Using TCP Wrappers

### Block a Host

Edit `/etc/hosts.deny`

```text
sshd: 192.168.1.100
```

### Allow Local Network

Edit `/etc/hosts.allow`

```text
sshd: 192.168.1.0/255.255.255.0
```

### Tasks

- Block SSH access from a specific host.
- Allow SSH access only from the local network.

---

## Lab 7 - Check AppArmor Status

### Command

```bash
sudo aa-status
```

### Tasks

- View loaded AppArmor profiles.
- Identify profiles in Enforce and Complain modes.

---

## Lab 8 - Switch AppArmor Modes

### Commands

```bash
sudo aa-enforce /etc/apparmor.d/*
sudo aa-complain /etc/apparmor.d/*
```

### Tasks

- Set profiles to Enforce mode.
- Switch profiles to Complain mode.

---

## Lab 9 - Reload AppArmor

### Commands

```bash
sudo systemctl reload apparmor
sudo systemctl start apparmor
```

### Tasks

- Reload AppArmor configuration.
- Verify the service is running.

---

## Skills Practiced

- Viewing firewall rules
- Creating firewall rules
- Allowing and blocking traffic
- IP-based filtering
- Custom iptables chains
- SSH access control
- AppArmor profile management
- Linux host-based security
