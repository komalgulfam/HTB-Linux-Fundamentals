# Automation

This file contains Linux automation using Bash scripts, Cron jobs, and Systemd Timers.

---

# Bash Script

| Command | Description |
|---------|-------------|
| `nano ~/script.sh` | Create a Bash script |
| `nano /home/USER/script.sh` | Create a Bash script |
| `#!/bin/bash` | Bash script header |
| `chmod +x script.sh` | Make script executable |

---

# Cron Jobs

| Command | Description |
|---------|-------------|
| `crontab -e` | Open cron editor |
| `* * * * * command` | Cron schedule format |
| `* * * * * /home/USER/script.sh > /home/USER/output.txt` | Run script every minute and save output |

### Cron Time Format

```
* * * * *
│ │ │ │ │
│ │ │ │ └── Day of Week
│ │ │ └──── Month
│ │ └────── Day of Month
│ └──────── Hour
└────────── Minute
```

---

# Systemd Timers

## Important Path

```
/etc/systemd/system
```

### Service File

```ini
[Unit]
Description=My Script

[Service]
ExecStart=/home/USER/script.sh
```

### Timer File

```ini
[Timer]
OnBootSec=5min
OnUnitActiveSec=1h

[Install]
WantedBy=timers.target
```

---

# Timer Commands

| Command | Description |
|---------|-------------|
| `sudo nano /etc/systemd/system/script.service` | Create service file |
| `sudo nano /etc/systemd/system/script.timer` | Create timer file |
| `sudo systemctl daemon-reload` | Reload systemd |
| `sudo systemctl enable script.timer` | Enable timer |
| `sudo systemctl start script.timer` | Start timer |
| `sudo systemctl status script.timer` | Check timer status |
