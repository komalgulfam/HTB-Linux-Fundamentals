# 08 - Storage

## Objective

Learn Linux storage management, including mounting and unmounting devices, configuring automatic mounts, managing swap space, enabling hibernation, changing file ownership, and creating symbolic links.

---

## Check Available Storage Devices

```bash
sudo fdisk -l
```

Lists all disks, partitions, and USB devices connected to the system.

---

## Mount a USB or Disk

```bash
sudo mount /dev/USBNAME ~/FOLDERINWHICHUSEEUSBDATA
```

Example:

```bash
sudo mount /dev/sdb1 ~/usb
```

---

## Unmount a Device

```bash
sudo umount /mnt/USBNAME
```

Example:

```bash
sudo umount /mnt/usb
```

---

## Bind Mount (Folder to Folder)

```bash
sudo mount --bind /home/asad/Desktop/FIRSTFILE /home/asad/Documents/SECONDFILE
```

Creates another mount point for the same directory.

---

## Configure Automatic Mounts

Edit the fstab file:

```bash
sudo nano /etc/fstab
```

Example for mounting a disk:

```text
USB/DISK    /home/USERNAME/FOLDER    none    ext4    0    0
```

Example for a bind mount:

```text
/home/USERNAME/FOLDER /home/USERNAME/FOLDER none bind 0 0
```

Changes take effect after reboot or remounting.

---

## Configure Swap Space

Create swap:

```bash
mkswap /dev/DRIVENAME
```

Enable swap:

```bash
sudo swapon /dev/DRIVENAME
```

Disable swap:

```bash
sudo swapoff /dev/DRIVENAME
```

Check swap status:

```bash
swapon --show
```

---

## Hibernation

Hibernate the system:

```bash
sudo systemctl hibernate
```

---

## Change File Ownership

Change owner and group:

```bash
sudo chown OWNER:GROUP FILE
```

Example:

```bash
sudo chown asad:users file.txt
```

Change only the owner:

```bash
sudo chown OWNER FILE
```

Example:

```bash
sudo chown asad file.txt
```

---

## Create a Symbolic Link

```bash
ln -s ~/FILE/FILE.txt CREATEFILENAME.txt
```

Example:

```bash
ln -s ~/Documents/data.txt data-link.txt
```

---

## Useful Storage Commands

Check storage devices:

```bash
sudo fdisk -l
```

Mount a device:

```bash
sudo mount /dev/sdb1 ~/usb
```

Unmount a device:

```bash
sudo umount /mnt/usb
```

Check active swap:

```bash
swapon --show
```

Change file owner:

```bash
sudo chown OWNER FILE
```

Create a symbolic link:

```bash
ln -s SOURCE TARGET
```

---

## What I Learned

- Viewed available storage devices.
- Mounted and unmounted disks and USB drives.
- Created bind mounts between directories.
- Configured automatic mounts using `/etc/fstab`.
- Created, enabled, and disabled swap space.
- Used system hibernation.
- Changed file ownership using `chown`.
- Created symbolic links using `ln -s`.
