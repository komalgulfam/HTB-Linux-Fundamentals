# 09 - File Transfer

## Objective

Learn different methods of transferring files between local and remote Linux systems using HTTP servers, `wget`, `rsync`, SSH, NFS, and symbolic links.

---

## File Sharing with Python HTTP Server

Start a simple HTTP server:

```bash
python3 -m http.server 6789
```

Or choose any port:

```bash
python3 -m http.server PORT
```

Access the shared files from another computer:

```
http://YOUR_IP:PORT
```

Download a file:

```bash
wget http://YOUR_IP:PORT/FILENAME
```

---

## HTTP Server using Node.js

Install:

```bash
npm install -g http-server
```

Start server:

```bash
http-server -p 8080
```

---

## PHP Web Server

Start a PHP server:

```bash
php -S YOUR_IP:8080
```

---

## Local File Transfer using rsync

Copy files:

```bash
rsync -av ~/SOURCE/file.txt ~/DESTINATION/file.txt
```

Mirror source (including deletions):

```bash
rsync -av --delete ~/SOURCE/ ~/DESTINATION/
```

---

## Remote File Transfer using rsync + SSH

Transfer files securely:

```bash
rsync -avz -e ssh --backup --backup-dir=~/backup --delete ~/SOURCE/ USER@REMOTE_IP:~/DESTINATION/
```

---

## Passwordless SSH Authentication

Generate SSH key:

```bash
ssh-keygen -t rsa -b 2048
```

Copy the public key:

```bash
ssh-copy-id USER@REMOTE_IP
```

---

## Network File System (NFS)

### Share a Folder

Edit exports file:

```bash
sudo nano /etc/exports
```

Example:

```text
/home/USERNAME/shared FRIEND_IP(rw,sync,no_subtree_check)
```

Apply changes:

```bash
sudo exportfs -ra
```

View exported folders:

```bash
sudo exportfs -v
```

Restart NFS:

```bash
sudo systemctl restart nfs-kernel-server
```

---

### Mount Shared Folder

```bash
sudo mount SERVER_IP:/home/USERNAME/shared ~/mountpoint
```

Unmount:

```bash
sudo umount ~/mountpoint
```

---

## Symbolic Links

Create a symbolic link:

```bash
ln -s ~/FILE/file.txt shortcut.txt
```

---

## Useful Commands

Show IP address:

```bash
ip addr
```

Show listening ports:

```bash
sudo netstat -tulnp
```

Test network connectivity:

```bash
ping -c 4 8.8.8.8
```

Trace packet route:

```bash
traceroute -I google.com
```

---

## What I Learned

- Shared files using Python HTTP Server.
- Used Node.js and PHP as lightweight web servers.
- Downloaded files with `wget`.
- Copied files locally using `rsync`.
- Transferred files securely over SSH using `rsync`.
- Configured passwordless SSH authentication.
- Shared directories using NFS.
- Mounted and unmounted remote NFS shares.
- Created symbolic links using `ln -s`.
- Verified network connectivity and listening services.
