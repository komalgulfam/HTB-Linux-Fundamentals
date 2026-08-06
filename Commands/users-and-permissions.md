# Users and Permissions

This file contains the Linux commands used for managing users, groups, ownership, and file permissions.

---

## User Management

| Command | Description |
|---------|-------------|
| `sudo useradd -m -s /bin/bash username` | Create a new user with a home directory and Bash shell |
| `sudo passwd username` | Set or change a user's password |
| `su - username` | Switch to another user |
| `sudo deluser username` | Delete a user |
| `sudo usermod --lock username` | Lock a user account |
| `sudo usermod --unlock username` | Unlock a user account |

---

## Group Management

| Command | Description |
|---------|-------------|
| `sudo addgroup groupname` | Create a new group |
| `sudo usermod -aG groupname username` | Add a user to a group |
| `sudo deluser username groupname` | Remove a user from a group |

---

## File Permissions

| Command | Description |
|---------|-------------|
| `chmod +x filename` | Make a file executable |
| `chmod permissions filename` | Change file permissions |

---

## File Ownership

| Command | Description |
|---------|-------------|
| `sudo chown owner filename` | Change the owner of a file |
| `sudo chown owner:group filename` | Change the owner and group of a file |

---

## Important Files

| File | Purpose |
|------|---------|
| `/etc/shadow` | Stores encrypted user passwords |
| `/etc/passwd` | Stores user account information |
| `/etc/group` | Stores group information |
