

# 🐧 Linux Commands — Complete Quick Notes (All Chapters)

---

# 1️⃣ Introduction

* Linux = Open-source OS
* Used in: **Servers, DevOps, Cloud, Containers, Security**
* Popular distros: Ubuntu, Amazon Linux, CentOS, RHEL, Debian

---

# 2️⃣ Linux Command Structure

```
command [options] [arguments]
```

Example:

```
ls -la /home
```

---

# 3️⃣ Linux File System Structure

```
/     → root
/home → user files
/etc  → configs
/var  → logs
/bin  → commands
/usr  → user programs
/tmp  → temp files
/root → root user
```

---

# 4️⃣ Basic Navigation Commands

```
pwd   → current path
ls    → list files
cd    → change directory
cd .. → back
cd ~  → home
clear -> for clear terminal
```

---

# 5️⃣ File & Directory Management

```
touch file.txt
mkdir test
rm file
rm -r folder
cp a b
mv old new
```

---

# 6️⃣ Viewing & Editing Files

```
cat file
less file
head file
tail file
nano file
vi file
```

---

# 7️⃣ File Permissions & Ownership

```
chmod 755 file
chown user:group file
```

Permission:

```
r → 4   w → 2   x → 1
```

---

# 8️⃣ Users & Groups Management

```
useradd name
passwd name
groupadd dev
usermod -aG dev name
```

---

# 9️⃣ System Information Commands

```
uname -a
hostname
uptime
free -h
df -h
top / htop
```

---

# 🔟 Process Management

```
ps -ef
top
kill PID
kill -9 PID
```

---

# 1️⃣1️⃣ Searching & Filtering

```
grep word file
find / -name file
locate file
```

---

# 1️⃣2️⃣ Networking Commands

```
ip a
ping google.com
netstat -tulnp
ss -tulnp
curl url
wget url
```

---

# 1️⃣3️⃣ Package Management (APT)

```
apt update
apt install nginx
apt remove nginx
apt upgrade
```

---

# 1️⃣4️⃣ Services & systemctl

```
systemctl start nginx
systemctl stop nginx
systemctl restart nginx
systemctl status nginx
systemctl enable nginx
```

---

# 1️⃣5️⃣ Archives & Compression

```
tar -cvf a.tar folder
tar -xvf a.tar
zip a.zip file
unzip a.zip
```

---

# 1️⃣6️⃣ Environment Variables

```
printenv
echo $PATH
export JAVA_HOME=/path
```

---

# 1️⃣7️⃣ Package Management (YUM / DNF)

```
yum install httpd
dnf install docker
```

---

# 1️⃣8️⃣ System Monitoring Commands

```
top
htop
vmstat
iostat
mpstat
watch df -h
```

---

# 1️⃣9️⃣ Log Files & Troubleshooting

```
/var/log/syslog
/var/log/auth.log
journalctl
journalctl -xe
```

---

# 2️⃣0️⃣ Cron Jobs & Task Scheduling

```
crontab -e
```

Format:

```
* * * * * command
```

Example:

```
0 2 * * * backup.sh
```

---

# 🏆 TOP 30 MOST IMPORTANT LINUX COMMANDS (Interview Must)

```
ls      cd      pwd
touch   mkdir   rm
cp      mv      cat
less    tail    grep
find    chmod   chown
ps      top     kill
df      free    uname
ping    curl    tar
systemctl crontab
```

---

# 💡 DEVOPS + CLOUD MUST-KNOW LINUX COMMANDS

```
ssh
scp
rsync
docker ps
kubectl get pods
terraform init
```

---
