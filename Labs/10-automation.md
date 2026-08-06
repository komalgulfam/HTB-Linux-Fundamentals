# 10 - Automation

## Objective

Learn how to automate tasks in Linux using Bash scripts, Cron Jobs, and Systemd timers to schedule and manage repeated tasks automatically.

---

## Bash Script Automation

Create a new script file:

```bash
nano script.sh
```

Add Bash header:

```bash
#!/bin/bash
```

Example:

```bash
#!/bin/bash

echo "Automation Task Running"
```

Make script executable:

```bash
chmod +x script.sh
```

Run script:

```bash
./script.sh
```

---

## Cron Jobs

Cron is used to schedule commands or scripts automatically at a specific time.

Open cron editor:

```bash
crontab -e
```

Cron format:

```text
* * * * * command
│ │ │ │ │
│ │ │ │ └── Day of week
│ │ │ └──── Month
│ │ └────── Day of month
│ └──────── Hour
└────────── Minute
```

Example: Run script every minute and save output:

```bash
* * * * * /home/USERNAME/script.sh > /home/USERNAME/result.txt
```

Common cron locations:

```bash
/etc/cron.d
/etc/cron.daily
/etc/cron.hourly
/etc/cron.weekly
```

---

## Systemd Timer Automation

Systemd timers are another method to automate tasks in Linux.

### Create Service File

Create a service:

```bash
sudo nano /etc/systemd/system/task.service
```

Example:

```ini
[Unit]
Description=Automation Task

[Service]
ExecStart=/home/USERNAME/script.sh
```

---

### Create Timer File

Create timer:

```bash
sudo nano /etc/systemd/system/task.timer
```

Example:

```ini
[Timer]
OnBootSec=5min
OnUnitActiveSec=1h

[Install]
WantedBy=timers.target
```

---

Reload systemd configuration:

```bash
sudo systemctl daemon-reload
```

Enable timer:

```bash
sudo systemctl enable task.timer
```

Start timer:

```bash
sudo systemctl start task.timer
```

Check timer status:

```bash
sudo systemctl status task.timer
```

---

## Creating Automation Script

Create script:

```bash
nano /home/USERNAME/task.sh
```

Example:

```bash
#!/bin/bash

date >> /home/USERNAME/output.txt
```

Give execution permission:

```bash
chmod +x /home/USERNAME/task.sh
```

---

## Useful Automation Tools

Install terminal animation tools:

```bash
sudo apt install cmatrix cbonsai cowsay
```

Matrix effect:

```bash
cmatrix
```

Terminal tree:

```bash
cbonsai
```

Display messages:

```bash
cowsay "Hello Linux"
```

---

## Environment Configuration

Change DNS configuration:

```bash
echo "nameserver 8.8.8.8" | sudo tee /etc/resolv.conf
```

---

## Useful Commands

Check running systemd services:

```bash
systemctl list-units --type=service
```

Check active timers:

```bash
systemctl list-timers
```

View system logs:

```bash
journalctl
```

---

## What I Learned

- Created Bash scripts for automation.
- Made scripts executable using `chmod +x`.
- Scheduled tasks using Cron Jobs.
- Learned Cron timing format.
- Created Systemd service files.
- Created Systemd timer files for automatic execution.
- Managed automated tasks using `systemctl`.
- Used Linux terminal automation tools like cmatrix, cbonsai, and cowsay.
- Learned how Linux can perform repeated tasks automatically without manual execution.
