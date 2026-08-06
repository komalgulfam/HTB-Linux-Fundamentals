# Networking Commands and Services

This file contains networking commands practiced during the Hack The Box Academy Linux Fundamentals module.

---

# Network Information

| Command | Description |
|---------|-------------|
| `ip addr` | Display IP addresses and network interfaces |
| `ip route` | Show the routing table |
| `sudo netstat -tulnp` | Show listening ports and active network services |
| `cat /etc/resolv.conf` | View configured DNS servers |

---

# Network Testing

| Command | Description |
|---------|-------------|
| `ping -c 4 8.8.8.8` | Test network connectivity |
| `traceroute -I google.com` | Show the path packets take to a destination |

---

# Interface Configuration

| Command | Description |
|---------|-------------|
| `sudo ifconfig eth0 down` | Disable a network interface |
| `sudo ifconfig eth0 up` | Enable a network interface |
| `sudo ip link set eth0 down` | Disable interface (modern command) |
| `sudo ip link set eth0 up` | Enable interface (modern command) |
| `sudo ifconfig eth0 <IP_ADDRESS>` | Assign a static IP address |
| `sudo ifconfig eth0 netmask 255.255.255.0` | Configure subnet mask |
| `sudo route add default gw <ROUTER_IP> eth0` | Set the default gateway |

---

# SSH

| Command | Description |
|---------|-------------|
| `sudo apt install openssh-server -y` | Install the OpenSSH server |
| `ssh username@IP_ADDRESS` | Connect to a remote system using SSH |
| `ssh-keygen -t rsa -b 2048` | Generate an SSH key pair |
| `ssh-copy-id username@IP_ADDRESS` | Copy SSH public key to a remote host |

---

# File Transfer

| Command | Description |
|---------|-------------|
| `rsync -av source destination` | Copy files locally while preserving attributes |
| `rsync -av --delete source destination` | Synchronize folders and remove deleted files |
| `rsync -avz -e ssh source username@IP:destination` | Securely synchronize files over SSH |
| `wget http://IP:PORT/file` | Download a file from a web server |

---

# Python HTTP Server

| Command | Description |
|---------|-------------|
| `python3 -m http.server` | Start a simple HTTP server |
| `python3 -m http.server 8080` | Start an HTTP server on port 8080 |
| `http://IP_ADDRESS:PORT` | Access the shared files from another machine |

---

# Web Servers

| Command | Description |
|---------|-------------|
| `sudo apt install apache2 -y` | Install Apache web server |
| `sudo systemctl start apache2` | Start Apache |
| `sudo systemctl status apache2` | Check Apache status |
| `php -S IP:PORT` | Start PHP development server |
| `http-server -p PORT` | Start a Node.js HTTP server |

---

# NFS (Network File System)

| Command | Description |
|---------|-------------|
| `sudo exportfs -ra` | Reload NFS exports |
| `sudo exportfs -v` | Display exported NFS shares |
| `sudo systemctl restart nfs-kernel-server` | Restart the NFS server |
| `sudo mount IP:/shared/folder ~/mountpoint` | Mount a remote NFS share |
| `sudo umount ~/mountpoint` | Unmount an NFS share |

---

# Common Ports

| Port | Service |
|------|---------|
| `21` | FTP |
| `22` | SSH |
| `80` | HTTP |
| `443` | HTTPS |
| `2049` | NFS |
| `3306` | MySQL |
| `8080` | Alternative HTTP |

---

## Notes

These commands were practiced during the Hack The Box Academy Linux Fundamentals module for learning Linux networking, remote access, file transfer, web services, and network troubleshooting.
