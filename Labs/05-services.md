# 05 - Services

## Objective
Learn how to manage Linux services using systemd and configure common network services.

---

## List System Services

```bash
systemctl list-units --type=service
```

Show only running services:

```bash
systemctl list-units --type=service --state=running
```

---

## Important systemd Directories

```
/etc/systemd/
/lib/systemd/
/usr/lib/systemd/
```

---

## Install OpenSSH Server

```bash
sudo apt install openssh-server -y
```

Check status:

```bash
systemctl status ssh
```

---

## Install Apache Web Server

```bash
sudo apt install apache2 -y
```

Start Apache:

```bash
sudo systemctl start apache2
```

Check status:

```bash
systemctl status apache2
```

---

## Python HTTP Server

Create a temporary web server:

```bash
python3 -m http.server 8080
```

Access it from another machine:

```
http://SERVER_IP:8080
```

---

## PHP Development Server

```bash
php -S IP_ADDRESS:PORT
```

Example:

```bash
php -S 192.168.1.10:8000
```

---

## Node.js HTTP Server

Install:

```bash
npm install -g http-server
```

Start server:

```bash
http-server -p 8080
```

---

## Useful Service Commands

Start a service:

```bash
sudo systemctl start SERVICE
```

Stop a service:

```bash
sudo systemctl stop SERVICE
```

Restart a service:

```bash
sudo systemctl restart SERVICE
```

Enable at boot:

```bash
sudo systemctl enable SERVICE
```

Disable at boot:

```bash
sudo systemctl disable SERVICE
```

Check status:

```bash
systemctl status SERVICE
```

Reload systemd:

```bash
sudo systemctl daemon-reload
```

---

## Common Ports

| Service | Port |
|---------|-----:|
| SSH | 22 |
| HTTP | 80 |
| HTTPS | 443 |
| FTP | 21 |
| MySQL | 3306 |
| NFS | 2049 |

---

## What I Learned

- Managed services using systemctl.
- Installed and started OpenSSH Server.
- Installed and managed Apache Web Server.
- Hosted files using Python HTTP Server.
- Started a PHP development server.
- Hosted files using Node.js http-server.
- Learned common service ports and systemd directories.
