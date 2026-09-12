# linux-practical-examination

## About This Project

This repository contains my Linux Practical Examination work completed as part of my Cloud DevOps course.

The practical demonstrates fundamental Linux commands and system administration concepts including file management, user and group management, file permissions, package management, Apache web server configuration, process management, text processing, and Linux networking.

---

## Skills Demonstrated

* Linux Command Line
* File and Directory Management
* File Content Operations
* Linux User Management
* Linux Group Management
* File Permissions and Ownership
* Package Management using YUM
* Apache Web Server
* Process Management
* Text Processing using `grep` and `sort`
* Linux Networking
* Basic Linux System Administration

---

# Practical Tasks

## Q1. Basic File Operations

Commands used:

```bash
mkdir linuxexam
cd linuxexam
touch student.txt course.txt result.txt
pwd
ls
```

This practical demonstrates creating directories and files and checking the current working directory and files.

---

## Q2. File Management

Commands used:

```bash
cp student.txt student_backup.txt
mv course.txt linux_course.txt
rm result.txt

mkdir documents backups scripts

mv linuxexam/student_backup.txt backups/
tree
```

This practical demonstrates copying, moving, deleting files, creating directories, and viewing the directory structure.

---

## Q3. File Content Operations

Commands used:

```bash
cat > student.txt
cat > linux_course.txt
cat student.txt
head -n 3 student.txt
tail -n 2 student.txt
wc student.txt
```

This practical demonstrates creating, viewing, and analyzing file contents.

---

## Q4. User Management

Commands used:

```bash
sudo useradd student01
sudo passwd student01
id student01
eval echo ~student01
su - student01
whoami
```

This practical demonstrates creating Linux users, setting passwords, checking user information, switching users, and verifying the current user.

---

## Q5. Group Management

Commands used:

```bash
sudo groupadd linuxbatch
sudo usermod -aG linuxbatch student01

sudo useradd student02
sudo usermod -aG linuxbatch student02

getent group linuxbatch
groups student01
```

This practical demonstrates creating groups and adding users to Linux groups.

---

## Q6. File Permissions

Commands used:

```bash
touch project.txt
sudo chmod 754 project.txt
ls -l

sudo chmod 640 project.txt
sudo chown student01 project.txt
sudo chgrp linuxbatch project.txt

ls -l project.txt
```

This practical demonstrates Linux file permissions, ownership, and group ownership.

---

## Q7. Permission Challenge

Commands used:

```bash
mkdir -p linuxexam/public linuxexam/private linuxexam/shared

sudo chmod 777 public
sudo chmod 700 private
sudo chmod 770 shared

ls -ld public private shared
```

This practical demonstrates applying different permissions to public, private, and shared directories.

---

## Q8. Package Management

Commands used:

```bash
sudo yum update
sudo yum install httpd -y
httpd -v

sudo systemctl start httpd
sudo systemctl status httpd
sudo systemctl enable httpd
sudo systemctl is-enabled httpd
```

This practical demonstrates package installation and managing the Apache HTTP Server service.

---

## Q9. Apache Web Server Configuration

Commands used:

```bash
sudo nano /etc/httpd/conf/httpd.conf

cd /var/www/html
sudo nano index.html

sudo systemctl restart httpd

curl http://<server-ip>
curl -i http://<server-ip>
```

This practical demonstrates Apache configuration, creating a webpage, restarting the web server, and testing the webpage using `curl`.

---

## Q10. Process Management

Commands used:

```bash
ps -ef
top
pgrep httpd
ps -p <PID> -f

sudo systemctl stop httpd
sudo systemctl status httpd

sudo systemctl start httpd
sudo systemctl status httpd
```

This practical demonstrates monitoring and managing Linux processes and services.

---

## Q11. Search and Text Processing

Commands used:

```bash
touch students.txt
nano students.txt

grep "vishal" students.txt
grep -i "a" students.txt
grep -i -c "a" students.txt

sort students.txt
sort -k2 students.txt
```

This practical demonstrates searching and processing text using `grep` and `sort`.

---

## Q12. Linux Networking

Commands used:

```bash
hostname
ip addr
ip link
ip route

ping google.com
ping -c 4 8.8.8.8

curl http://<server-ip>
nslookup <domain>

sudo ss -tulnp
```

This practical demonstrates basic Linux networking, IP configuration, routing, connectivity testing, DNS lookup, and checking listening ports.


# Repository Contents

```text
linux-practical-examination/
│
├── README.md
├── Linux-Practical-Examination-Report.pdf
│
└── screenshots/
    ├── q01-file-operations.png
    ├── q02-file-management.png
    ├── q03-file-content.png
    ├── q04-user-management.png
    ├── q05-group-management.png
    ├── q06-file-permissions.png
    ├── q07-permission-challenge.png
    ├── q08-package-management.png
    ├── q09-apache-web-server.png
    ├── q10-process-management.png
    ├── q11-text-processing.png
    └── q12-networking.png


---



# Learning outcome :

Through this practical examination, I gained hands-on experience with Linux command-line operations and basic system administration.

The practical helped me understand how Linux systems handle files, users, groups, permissions, packages, services, processes, text processing, and networking.
