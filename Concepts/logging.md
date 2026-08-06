# Linux Logging

## What is Logging?

Logging is the process of recording events that happen on a Linux system.

Logs help administrators monitor system activity, troubleshoot problems, detect security incidents, and audit user actions.

---

## Why Logs are Important?

Logs are useful for:

- Troubleshooting system issues
- Detecting failed logins
- Monitoring services
- Auditing user activity
- Tracking hardware events
- Security analysis

---

## Traditional Log Files

Older Linux systems store logs in the `/var/log` directory.

Common log files include:

| Log File | Purpose |
|----------|---------|
| /var/log/syslog | General system events |
| /var/log/auth.log | Authentication and SSH logs |
| /var/log/kern.log | Kernel messages |
| /var/log/dmesg | Boot and hardware messages |

---

## systemd Journal

Modern Linux distributions use **systemd-journald** to collect logs.

Logs can be viewed using:

- journalctl
- journalctl -k
- journalctl -u SERVICE
- journalctl _COMM=sudo

The journal stores logs from:

- Kernel
- Services
- Applications
- User actions
- Boot process

---

## Kernel Logs

Kernel logs contain information about:

- Hardware detection
- USB devices
- Drivers
- Memory
- CPU
- Boot process

These logs help diagnose hardware-related problems.

---

## Service Logs

Each service generates its own logs.

Examples:

- SSH
- Docker
- Apache
- NetworkManager

Service logs help identify why a service failed or stopped.

---

## Authentication Logs

Authentication logs record:

- User login attempts
- SSH logins
- sudo commands
- Failed password attempts

These logs are useful during security investigations.

---

## Log Rotation

Logs continuously grow in size.

Linux uses **logrotate** to:

- Archive old logs
- Compress logs
- Delete very old logs
- Prevent disks from filling up

---

## Journal vs Traditional Logs

| Traditional Logs | Journal |
|------------------|----------|
| Stored in text files | Stored in systemd journal |
| Located in /var/log | Accessed with journalctl |
| Separate files | Centralized logging |

---

## Important Concepts

- Logs record system events.
- `/var/log` stores traditional log files.
- `journalctl` is used on modern Linux systems.
- Kernel logs are different from authentication logs.
- Service logs help troubleshoot applications.

---

## Exam Notes

Remember:

- `/var/log` → Traditional logs
- `journalctl` → systemd logs
- `journalctl -k` → Kernel logs
- `journalctl -u ssh` → SSH service logs
- `journalctl _COMM=sudo` → sudo activity
