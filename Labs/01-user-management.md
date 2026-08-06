# Lab 01 - User Management

## Objective

Learn how to create, manage, and secure Linux users and groups.

---

## Environment

- Operating System: Kali Linux
- Shell: Bash
- Privileges: sudo

---

## Tasks Performed

### 1. Created a New User

```bash
sudo useradd -m -s /bin/bash testuser
```

**Result**

- A new user account was created.
- A home directory was automatically generated.

---

### 2. Set a Password

```bash
sudo passwd testuser
```

**Result**

- Password successfully assigned.

---

### 3. Switched to the New User

```bash
su - testuser
```

**Result**

- Logged into the newly created account.

---

### 4. Created a New Group

```bash
sudo addgroup developers
```

**Result**

- A new group named `developers` was created.

---

### 5. Added User to the Group

```bash
sudo usermod -a -G developers testuser
```

**Result**

- User became a member of the `developers` group.

---

### 6. Locked the User Account

```bash
sudo usermod --lock testuser
```

**Result**

- Login for the user was disabled.

---

### 7. Unlocked the User Account

```bash
sudo usermod --unlock testuser
```

**Result**

- User was able to log in again.

---

### 8. Viewed Password Information

```bash
sudo cat /etc/shadow
```

**Observation**

- Password hashes are stored in `/etc/shadow`.
- Only the root user can access this file.

---

## Commands Used

```text
useradd
passwd
su
addgroup
usermod
cat /etc/shadow
```

---

## What I Learned

- How to create Linux users.
- How to assign passwords.
- How to create and manage groups.
- How to lock and unlock user accounts.
- Why `/etc/shadow` is important for password security.

---

## Screenshots

- User creation
- Password setup
- Group assignment
- Locked account
- `/etc/shadow` output
