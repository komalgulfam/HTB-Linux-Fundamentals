# Storage Management

This file contains storage and disk management commands practiced during the Hack The Box Academy Linux Fundamentals module.

---

# Disk Information

| Command | Description |
|---------|-------------|
| `sudo fdisk -l` | List all available disks and partitions |

---

# Mounting

| Command | Description |
|---------|-------------|
| `sudo mount /dev/DEVICE ~/mountpoint` | Mount a storage device |
| `sudo umount ~/mountpoint` | Unmount a mounted device |
| `sudo mount --bind source destination` | Bind mount one directory to another |

---

# Automatic Mounting

Configuration file:

```text
/etc/fstab
```

Example:

```text
DEVICE   /mountpoint   ext4   defaults   0   0
```

Bind mount example:

```text
/home/user/source  /home/user/destination  none  bind  0  0
```

---

# Swap Memory

| Command | Description |
|---------|-------------|
| `mkswap /dev/DEVICE` | Create swap space |
| `sudo swapon /dev/DEVICE` | Enable swap |
| `sudo swapoff /dev/DEVICE` | Disable swap |
| `swapon --show` | Display active swap devices |

---

# Hibernation

| Command | Description |
|---------|-------------|
| `systemctl hibernate` | Hibernate the system |
| `sudo systemctl hibernate` | Hibernate with administrator privileges |

---

# Symbolic Links

| Command | Description |
|---------|-------------|
| `ln -s source_file link_name` | Create a symbolic (soft) link |

---

# File Ownership

| Command | Description |
|---------|-------------|
| `sudo chown owner file` | Change file owner |
| `sudo chown owner:group file` | Change file owner and group |

---

## Skills Practiced

- Disk management
- Mounting and unmounting
- Automatic mounting with fstab
- Swap memory configuration
- Hibernation
- Symbolic links
- File ownership management
