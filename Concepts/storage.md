# Storage

## What is Storage?

Storage woh jagah hai jahan operating system aur user ka data permanently save hota hai.

Examples:
- HDD (Hard Disk Drive)
- SSD (Solid State Drive)
- USB Drive
- External Hard Disk

---

## Mounting

Linux mein storage device ko use karne se pehle usse filesystem ke kisi folder ke sath connect kiya jata hai.

Is process ko **Mounting** kehte hain.

Example:

USB → /mnt/usb

Ab USB ka sara data `/mnt/usb` folder se access hoga.

---

## Unmounting

Jab storage device ki zarurat na ho to usse safely disconnect kiya jata hai.

Is process ko **Unmounting** kehte hain.

Unmount karne ke baad system us device ko access nahi karta.

---

## Bind Mount

Bind mount mein ek existing folder ko kisi doosre folder par mount kiya jata hai.

Example:

/home/asad/Desktop/Data

↓

/home/asad/Documents/Data

Dono locations same files show karti hain.

---

## Automatic Mount (fstab)

Agar har boot ke baad manually mount na karna ho to `/etc/fstab` use hota hai.

System boot hote hi listed devices automatically mount ho jati hain.

---

## Swap Space

Swap disk ka ek hissa hota hai jo RAM ki tarah use hota hai.

Jab RAM full ho jaye to Linux temporary data swap space mein bhej deta hai.

Advantages:
- Low memory situations handle hoti hain.
- System immediately crash nahi karta.

Disadvantage:
- Disk RAM se slow hoti hai.
- Performance kam ho sakti hai.

---

## Hibernation

Hibernation mein RAM ka sara data disk par save kar diya jata hai aur system completely power off ho jata hai.

Next boot par wahi previous session restore ho jata hai.

Difference:

Sleep
- RAM powered rehti hai.
- Thodi electricity use hoti hai.

Hibernation
- RAM ka data disk par save hota hai.
- Computer completely off hota hai.
- Power consume nahi hoti.

---

## Storage Devices

Linux disks ko files ki tarah treat karta hai.

Examples:

- /dev/sda
- /dev/sdb
- /dev/nvme0n1

Partitions:

- /dev/sda1
- /dev/sda2

---

## Filesystem

Filesystem decide karta hai ke disk par files kis tarah store hongi.

Common Linux filesystems:

- ext4
- xfs
- btrfs

Windows:

- NTFS
- FAT32
- exFAT

---

## Storage Commands Used

HTB Linux Fundamentals mein storage ke liye mainly ye commands use hui:

- fdisk
- mount
- umount
- mkswap
- swapon
- swapoff

In commands ki details `Commands/storage.md` mein hain.
