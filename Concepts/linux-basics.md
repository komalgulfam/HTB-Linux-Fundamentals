# Linux Basics

## What is Linux?

Linux is a free and open-source operating system based on the Linux kernel. It is widely used in servers, cloud computing, embedded systems, cybersecurity, and personal computers due to its stability, security, and flexibility.

---

## Key Features

- Open Source
- Secure
- Stable
- Multi-user
- Multitasking
- Portable
- Highly customizable

---

## Linux Architecture

Linux consists of four main layers:

```
Applications
      │
      ▼
    Shell
      │
      ▼
    Kernel
      │
      ▼
   Hardware
```

### Hardware

The physical components of the computer such as the CPU, RAM, hard drive, keyboard, and network card.

### Kernel

The kernel is the core of the operating system. It acts as a bridge between software and hardware.

**Responsibilities**

- Process management
- Memory management
- Device management
- File system management
- Networking

### Shell

The shell is a command-line interface that allows users to communicate with the Linux kernel.

Common shells:

- Bash
- Zsh
- Fish

### Applications

Applications are programs that run on top of the operating system, such as Firefox, VS Code, Apache, or Docker.

---

## Linux File System

Linux uses a hierarchical file system that starts from the **Root Directory (/)**.

### Common Directories

| Directory | Purpose |
|-----------|---------|
| `/` | Root directory |
| `/bin` | Essential commands |
| `/boot` | Boot files |
| `/dev` | Device files |
| `/etc` | Configuration files |
| `/home` | User home directories |
| `/lib` | Shared libraries |
| `/mnt` | Temporary mount point |
| `/opt` | Optional software |
| `/proc` | Process and kernel information |
| `/sbin` | System administration commands |
| `/tmp` | Temporary files |
| `/usr` | User applications |
| `/var` | Logs, cache, and variable data |

---

## Linux Users

### Root User

- UID = 0
- Has complete administrative privileges.

### Regular User

- Has limited permissions.
- Used for daily tasks.

---

## File Permissions

Linux uses three basic permissions:

- Read (r)
- Write (w)
- Execute (x)

Permissions are assigned to:

- Owner
- Group
- Others

---

## Processes

A process is a running instance of a program.

Each process has a unique **Process ID (PID)**.

---

## Services

A service is a background process that performs specific tasks for the operating system.

Examples:

- SSH
- Apache
- Docker
- MySQL

---

## Package Managers

Different Linux distributions use different package managers.

| Distribution | Package Manager |
|-------------|-----------------|
| Ubuntu / Debian | apt |
| Fedora / RHEL | dnf |
| CentOS | yum |
| Arch Linux | pacman |

---

## Important Linux Concepts

- Linux is case-sensitive.
- Everything is treated as a file.
- Multiple users can work simultaneously.
- Most configuration files are stored in `/etc`.
- Logs are usually stored in `/var/log` or accessed using `journalctl`.

---

## Summary

- Linux is a secure and open-source operating system.
- The kernel manages hardware resources.
- The shell provides an interface between the user and the kernel.
- Everything in Linux begins from the root directory (`/`).
- Linux supports multiple users, multitasking, and strong permission management.
