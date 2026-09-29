
# Linux Users and Groups Management

## Objective

Manage Linux users and groups by creating users, modifying user accounts, assigning group membership, deleting users, and configuring sudo access.

---

## Step 1: Create a User

```bash
useradd user1
```

### What it does

Creates a new Linux user account named `user1`.

### Verify

```bash
id user1
```

Displays the user's UID, GID, and group membership.

---

## Step 2: Set User Password

```bash
passwd user1
```

### What it does

Sets or changes the password for `user1`.

---

## Step 3: renaming username

```bash
usermod -l "Linux User" user1
```

### What it does


renaming username from old to new

---

## Step 4: Create a Group

```bash
groupadd developers
```

### What it does

Creates a new group named `developers`.

---

## Step 5: Add User to a Group

```bash
usermod -aG developers user1
```

### What it does

Adds `user1` to the `developers` supplementary group.

* `-a` → Append
* `-G` → Supplementary groups

### Verify

```bash
groups user1
```

---

## Step 6: Remove a User

```bash
userdel user1
```

### What it does

Deletes the user account from the system.

---

## Step 7: Configure Sudo Access

Add the user to the administrative group.

### RHEL/CentOS/Rocky/AlmaLinux

```bash
usermod -aG wheel user1
```

### Ubuntu/Debian

```bash
usermod -aG sudo user1
```

### What it does

Allows the user to execute administrative commands through `sudo`, subject to the system's sudo configuration.

---

## Step 8: Verify User and Group Information

```bash
id user1
```

```bash
groups user1
```

```bash
getent passwd user1
```

```bash
getent group developers
```

---

## User Management Workflow

```text
Create User
    ↓
Set Password
    ↓
Create Group
    ↓
Add User to Group
    ↓
Configure Sudo Access
    ↓
Verify User & Groups
    ↓
Modify / Delete User
```

## Result

Successfully practiced Linux user and group administration, including account creation, modification, deletion, group membership, and sudo access.
