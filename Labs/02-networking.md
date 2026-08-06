# 02 - Networking Lab

## Objective
Learn basic Linux networking, IP configuration, DNS, routing, connectivity testing, and simple file sharing.

---

## Lab 1 - Display Network Information

### Commands
```bash
ip addr
ip route
```

### Tasks
- View IP address.
- Identify the network interface.
- Find the default gateway.

---

## Lab 2 - Configure DNS

### Command
```bash
echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf
```

### Tasks
- Change DNS server.
- Verify internet connectivity.

---

## Lab 3 - Test Network Connectivity

### Commands
```bash
ping -c 4 8.8.8.8
ping -c 4 google.com
```

### Tasks
- Test internet connection.
- Verify DNS resolution.

---

## Lab 4 - Trace Network Route

### Command
```bash
traceroute -I google.com
```

### Tasks
- Observe routers between the local machine and destination.

---

## Lab 5 - Configure a Static IP

### Commands
```bash
sudo ifconfig eth0 192.168.1.100
sudo ifconfig eth0 netmask 255.255.255.0
sudo route add default gw 192.168.1.1 eth0
```

### Tasks
- Assign a static IP.
- Configure subnet mask.
- Set the default gateway.

---

## Lab 6 - Enable and Disable Network Interface

### Commands
```bash
sudo ip link set eth0 down
sudo ip link set eth0 up
```

### Tasks
- Disable the interface.
- Enable the interface again.

---

## Lab 7 - View Listening Ports

### Command
```bash
sudo netstat -tulnp
```

### Tasks
- Identify running network services.
- Check listening ports.

---

## Lab 8 - Share Files Using Python HTTP Server

### Server
```bash
python3 -m http.server 8080
```

### Client
```
http://SERVER_IP:8080
```

### Tasks
- Start a web server.
- Access shared files from another computer.

---

## Lab 9 - Download Files with wget

### Command
```bash
wget http://SERVER_IP:8080/file.txt
```

### Tasks
- Download files from another Linux machine.

---

## Skills Practiced

- IP addressing
- Default gateway configuration
- DNS configuration
- Network troubleshooting
- Connectivity testing
- Static IP configuration
- Port inspection
- Simple HTTP file sharing
