# DAY-01: LINUX, SHELL SCRIPTING AND GIT

Goal: Command-line mastery, Git operations, GitHub workflows

✅ Advanced Linux CLI (file ops, grep, sed, awk, systemctl, crontab)

✅ User management, permissions, networking commands

✅ Git advanced: branching, rebase, stash, cherry-pick, tags

✅ GitHub Actions basics: workflows, triggers, jobs

Hands-on:

- Write Linux scripts (e.g., backup script, monitor disk usage)

- Create and manage a GitHub repo

- Automate a workflow with GitHub Actions


**Day 1** of your 7-day DevOps mastery journey and the focus is **Linux & Shell Scripting**, we’ll go deep into the **core areas that DevOps engineers use daily**.

---

## ✅ **Day 1: Linux & Shell Scripting – Full Plan (10 Hours)**

### 🔹 **1. Linux Basics Refresher (1.5 hrs)**
Even if you know these, go deep into:
- Filesystem structure: `/etc`, `/var`, `/opt`, `/home`, `/proc`, `/tmp`, `/dev`
- Basic commands: `ls`, `cd`, `cp`, `mv`, `rm`, `mkdir`, `rmdir`, `touch`, `cat`, `more`, `less`, `head`, `tail`
- Path management: `.` vs `..` vs `~`
- Absolute vs relative paths

📘 **Practice**:  
Explore folders using `cd`, `tree`, and `find`. Try:
```bash
find /etc -name "*.conf" | head -10
```

---

### 🔹 **2. File Permissions & User Management (1.5 hrs)**
- Users and groups: `adduser`, `usermod`, `passwd`, `groups`, `id`
- File permissions: `r`, `w`, `x`, numeric (`chmod 755`), symbolic (`chmod u+x`)
- Ownership: `chown`, `chgrp`
- `sudo` and `/etc/sudoers` (`visudo`)

📘 **Practice**:
```bash
sudo adduser devopsuser
sudo usermod -aG sudo devopsuser
chmod 755 myscript.sh
```

---

### 🔹 **3. Essential Linux Tools (2 hrs)**
- Networking: `ip a`, `ping`, `netstat`, `ss`, `curl`, `wget`, `nslookup`
- Processes: `top`, `htop`, `ps`, `kill`, `killall`, `nice`
- Disk usage: `df -h`, `du -sh`, `lsblk`, `mount`, `umount`
- Package managers:
  - Debian/Ubuntu: `apt`
  - RHEL/CentOS: `yum`, `dnf`

📘 **Practice**:
```bash
df -h
du -sh /var/log/*
ps aux | grep nginx
```

---

### 🔹 **4. Shell Scripting Fundamentals (3 hrs)**
> Bash is the most used scripting shell in DevOps

**Topics**:
- `#!/bin/bash`, making script executable
- Variables and quoting
- Conditions: `if`, `else`, `elif`
- Loops: `for`, `while`
- Functions
- Arguments: `$1`, `$@`, `$#`
- Exit codes, `set -e`, `trap`

📘 **Example 1: Check Disk Usage**
```bash
#!/bin/bash
THRESHOLD=80
USAGE=$(df -h / | grep '/' | awk '{ print $5 }' | sed 's/%//g')

if [ $USAGE -gt $THRESHOLD ]; then
  echo "Disk usage is above threshold: $USAGE%"
fi
```

📘 **Example 2: Basic for loop**
```bash
for file in *.log; do
  echo "Compressing $file"
  gzip "$file"
done
```

---

### 🔹 **5. Cron Jobs & Systemd (1 hr)**
- Schedule tasks using `crontab -e`
  ```
  */5 * * * * /home/user/myscript.sh
  ```
- Understand `systemctl`, `systemd` services
  - Start/stop services
  - Create custom service files

---

### 🔹 **6. Practice Tasks / Assignments (1 hr)**
🛠️ Try to implement:
- A backup script: tar + compress `/etc` to `/backup/` folder
- A log rotation script (move and gzip old logs)
- A system health script:
  - Show CPU usage, memory usage, disk usage, and top 5 processes

---

## 🎯 Output by End of Day 1:
- [ ] Mastered basic + advanced Linux commands
- [ ] Comfortable with user, permission, and file ops
- [ ] Wrote 3-4 shell scripts (disk check, log cleanup, backup)
- [ ] Scheduled a job using `cron`
- [ ] Documented learnings in a Markdown file

---


echo "# abcd" >> README.md

git init

git add README.md

git commit -m "first commit"

git branch -M main

git remote add origin https://github.com/tirucloud/abcd.git

git push -u origin main

## git commands

git init ---> it creates .git folder

git status

git add -A

git commit -m "message"

git branch -M main

git pus
