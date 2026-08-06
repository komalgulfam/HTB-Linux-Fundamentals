# 04 - Logging Lab

## Objective

Learn how to inspect Linux log files, use `journalctl`, and monitor system events for troubleshooting and security.

---

## Lab 1 - View Log Directory

### Command

```bash
ls /var/log
```

### Tasks

- List available log files.
- Identify common system log locations.

---

## Lab 2 - View All System Logs

### Command

```bash
journalctl
```

### Tasks

- Display all system logs.
- Scroll through historical log entries.

---

## Lab 3 - View Sudo Logs

### Command

```bash
journalctl _COMM=sudo
```

### Tasks

- Display commands executed using `sudo`.
- Review privilege escalation events.

---

## Lab 4 - View Kernel Logs

### Command

```bash
journalctl -k
```

### Tasks

- Display kernel messages.
- Identify hardware and driver events.

---

## Lab 5 - View SSH Logs

### Command

```bash
journalctl -u ssh
```

### Tasks

- Display SSH service logs.
- Review login attempts and SSH activity.

---

## Lab 6 - Monitor Logs in Real Time

### Command

```bash
journalctl -fx
```

### Tasks

- Monitor new log entries as they occur.
- Observe system events while performing actions.

---

## Lab 7 - Generate Log Entries

### Commands

```bash
sudo ls /root
sudo iptables -L
sudo systemctl status ssh
```

### Tasks

- Execute privileged commands.
- Verify that new entries appear in the journal.

---

## Lab 8 - Examine Traditional Log Files

### Commands

```bash
cat /var/log/syslog
cat /var/log/auth.log
cat /var/log/kern.log
```

### Tasks

- View system logs.
- Review authentication logs.
- Review kernel logs.

---

## Skills Practiced

- Exploring Linux log files
- Using journalctl
- Monitoring logs in real time
- Reviewing sudo activity
- Investigating SSH logs
- Inspecting kernel messages
- Basic system troubleshooting
- Log analysis
