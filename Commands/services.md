# Services

This file contains commands related to Linux services (systemd), SSH, Apache, and service management.

---

# Service Management

| Command | Description |
|---------|-------------|
| `systemctl list-units --type=service` | List all services |
| `systemctl list-units --type=service --state=running` | Show only running services |
| `sudo systemctl start SERVICE` | Start a service |
| `sudo systemctl stop SERVICE` | Stop a service |
| `sudo systemctl restart SERVICE` | Restart a service |
| `sudo systemctl reload SERVICE` | Reload a service |
| `sudo systemctl enable SERVICE` | Enable service at boot |
| `sudo systemctl disable SERVICE` | Disable service at boot |
| `sudo systemctl status SERVICE` | Check service status |
| `sudo systemctl daemon-reload` | Reload systemd configuration |

---

# Systemd Paths

| Path | Description |
|------|-------------|
| `/etc/systemd` | Local systemd configuration |
| `/lib/systemd` | Default systemd files |
| `/usr/lib/systemd` | Systemd service files |

---

# SSH Server

| Command | Description |
|---------|-------------|
| `sudo apt install openssh-server -y` | Install OpenSSH server |
| `sudo systemctl start ssh` | Start SSH service |
| `sudo systemctl status ssh` | Check SSH service status |

---

# Apache Web Server

| Command | Description |
|---------|-------------|
| `sudo apt install apache2 -y` | Install Apache |
| `sudo systemctl start apache2` | Start Apache |
| `sudo systemctl restart apache2` | Restart Apache |
| `sudo systemctl reload apache2` | Reload Apache |
| `sudo systemctl status apache2` | Check Apache status |

---

# AppArmor

| Command | Description |
|---------|-------------|
| `sudo systemctl start apparmor` | Start AppArmor |
| `sudo systemctl reload apparmor` | Reload AppArmor |
| `sudo aa-status` | Show AppArmor status |
| `sudo aa-enforce /etc/apparmor.d/*` | Set profiles to enforce mode |
| `sudo aa-complain /etc/apparmor.d/*` | Set profiles to complain mode |
