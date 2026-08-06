# 07 - Linux Containers (LXC)

## Objective

Learn the basics of Linux Containers (LXC) by installing LXC, creating containers, starting/stopping them, entering containers, and managing their resources.

---

## Install LXC

```bash
sudo apt update && sudo apt install lxc lxc-templates -y
```

---

## Create a Container

```bash
sudo lxc-create -n CONTAINERNAME -t download -- -d OSNAME -r VERSION -a amd64
```

Example:

```bash
sudo lxc-create -n ubuntu-test -t download -- -d ubuntu -r 22.04 -a amd64
```

---

## List Containers

```bash
sudo lxc-ls -f
```

---

## Start a Container

```bash
sudo lxc-start -n CONTAINERNAME
```

Example:

```bash
sudo lxc-start -n ubuntu-test
```

---

## Enter a Container

```bash
sudo lxc-attach -n CONTAINERNAME
```

Example:

```bash
sudo lxc-attach -n ubuntu-test
```

Exit the container:

```bash
exit
```

---

## Stop a Container

```bash
sudo lxc-stop -n CONTAINERNAME
```

---

## Configure Resource Limits

Edit the default configuration:

```bash
sudo nano /etc/lxc/default.conf
```

Example configuration:

```ini
lxc.cgroup2.cpu.weight = 512
lxc.cgroup2.memory.max = 512M
```

- `cpu.weight` → CPU priority
- `memory.max` → Maximum RAM

---

## Restart LXC

```bash
sudo systemctl restart lxc
```

Reload systemd if needed:

```bash
sudo systemctl daemon-reload
```

---

## Useful LXC Commands

List containers:

```bash
sudo lxc-ls -f
```

Start a container:

```bash
sudo lxc-start -n CONTAINERNAME
```

Enter a container:

```bash
sudo lxc-attach -n CONTAINERNAME
```

Stop a container:

```bash
sudo lxc-stop -n CONTAINERNAME
```

---

## What I Learned

- Installed LXC on Linux.
- Created Linux containers from downloadable templates.
- Listed available containers.
- Started and stopped containers.
- Entered containers using `lxc-attach`.
- Configured CPU and memory limits.
- Restarted the LXC service after configuration changes.
