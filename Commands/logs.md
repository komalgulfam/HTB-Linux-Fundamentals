# Linux Logs

This file contains the log analysis and file monitoring commands practiced during the Hack The Box Academy Linux Fundamentals module.

---

# System Logs

| Command | Description |
|---------|-------------|
| `ls /var/log` | List available log files |
| `journalctl` | Display all system logs |
| `journalctl -k` | Show kernel logs |
| `journalctl -u ssh` | Show SSH service logs |
| `journalctl _COMM=sudo` | Show logs related to sudo commands |
| `journalctl -fx` | Follow new log entries in real time |

---

# Log Directories

| Path | Description |
|------|-------------|
| `/var/log` | Main directory containing system log files |

---

# File Monitoring

| Command | Description |
|---------|-------------|
| `lsof` | List open files and the processes using them |
| `lsof | grep filename` | Find which process is using a specific file |

---

# Common Use Cases

| Task | Command |
|------|---------|
| View all logs | `journalctl` |
| View kernel logs | `journalctl -k` |
| View SSH logs | `journalctl -u ssh` |
| View sudo activity | `journalctl _COMM=sudo` |
| Monitor new log entries | `journalctl -fx` |
| Check open files | `lsof` |

---

## Notes

These commands were practiced to understand Linux logging, system monitoring, and how to identify processes using files.
