##  🖥️  Linux Architecture

<img src="https://github.com/user-attachments/assets/3bc7cf1e-7540-4eda-8b5a-2a39086eaf9f" alt="Image" width="300"/>

- Application -> Shell -> Kernel -> Hardware
- E.g. To create a new folder

---

## What is Bootloader?
- A **bootloader** is a small program that starts your operating system when you turn on your computer or device.
- E.g. GRUB (GRand Unified Bootloader)
- Mostly used command Ctrl + r = to see previous commands which were entered in terminal

---

## 🧾 Basic Linux Commands (with Examples)

| Command                          | Description                                      |
|----------------------------------|--------------------------------------------------|
| `free -h`                        | RAM usage in human-readable format               |
| `df -h`                          | Disk space usage                                 |
| `top`                            | Live view of CPU and memory                      |
| `cd /`                           | Go to root directory                             |
| `ls`                             | List files and directories                       |
| `ls -l` / `ls -ltr`              | Detailed file list / with recent files last      |
| `date`                           | Show current date and time                       |
| `mkdir folder`                   | Create new folder                                |
| `pwd`                            | Show current working directory                   |
| `touch file.txt`                 | Create a new file                                |
| `cd ..`                          | Go back to parent directory                      |
| `rm file.txt`                    | Delete a file                                    |
| `rmdir folder`                   | Delete an empty folder                           |
| `echo "Hello" > file.txt`        | Write text to a file                             |
| `head file.txt` / `tail file.txt`| View start/end of file                           |
| `tail -f file.txt`               | 📡 Shows last lines and updates live             |
| `less file.txt` / `more file.txt`| View file page-by-page                           |
| `cp file folder/`                | Copy file to folder                              |
| `cp -r folder1 folder2`          | Copy entire directory                            |
| `mv file1 file2`                 | Move or rename a file                            |
| `wc file.txt`                    | Word, line, and byte count                       |
| `ln file.txt hardlink.txt`       | Create a hard link                               |
| `ln -s file.txt softlink.txt`    | Create a soft link (symbolic link)               |
| `cut -b 1-4 file.txt`            | Show specific bytes from each line               |
| `echo "Om" \| tee file.txt`      | Print and save output to file                    |
| `sort file.txt`                  | Sort file content                                |
| `diff file1.txt file2.txt`       | Show differences between two files               |
| `ps`                             | View running processes                           |
| `kill PID`                       | Terminate a process                              |
| `nohup command &`                | Run command in background, log output            |
| `vmstat` / `vmstat -a`           | Show virtual memory stats                        |

---

## Hardlink and Softlink
🔗 **Hard Link**
- A copy of the file that points to the same data on disk.
- Even if you delete the original file, the hard link still works.
- 📌 Think of it like: Two names for one file.
- Command : ln original.txt hardlink.txt

🔗 **Soft Link**
- A shortcut or pointer to another file (like Windows shortcuts).
- If you delete the original file, the soft link breaks.
- 📌 Think of it like: A signboard pointing to another file.
- Command : ln -s original.txt  softlink.txt

🧠 **Summary Table:**

| Action                            | Hard Link         | Soft Link        |
|----------------------------------|-------------------|------------------|
| Original file is updated         | ✅ Reflects        | ✅ Reflects       |
| Original file is deleted         | ✅ Still works     | ❌ Broken         |
| Original is deleted & recreated  | ❌ New file ignored | ❌ Broken         |

---
### **Users and File management**
 **Sytem level commands**

| Command                                 | Description                                         |
|-----------------------------------------|-----------------------------------------------------|
| `uname`                                 | Shows platform/system name                          |
| `uptime`                                | Shows system uptime and user sessions               |
| `date`                                  | Displays current date and time                      |
| `who`                                   | Shows all active user sessions                      |
| `whoami`                                | Shows the current logged-in username                |
| `which`                                 | Shows path of a command or application              |
| `id`                                    | Displays UID, GID, and group info of current user   |
| `sudo shutdown`                         | Shuts down the system                               |
| `sudo reboot`                           | Restarts the system                                 |
| `sudo apt-get update`                   | Updates package lists (Debian/Ubuntu)               |
| `sudo apt-get install docker.io`        | Installs Docker                                     |
| `sudo apt remove docker.io`             | Removes Docker                                      |
| `sudo useradd -m Shubham`               | Creates a new user with home directory              |
| `sudo passwd Shubham`                   | Sets a password for user `Shubham`                  |
| `su Shubham`                            | Switches to user `Shubham`                          |
| `exit`                                  | Returns to previous/primary user                    |
| `sudo userdel Shubham`                  | Deletes user `Shubham`                              |
| `sudo groupadd tester`                  | Creates a new group called `tester`                 |
| `sudo gpasswd -a Shubham tester`        | Adds user to group (use `-m` for multiple users)    |
| `sudo groupdel tester`                  | Deletes the group `tester`                          |


 ## **File permission commands**
 - drwxrwxr -> d means directory,first pair rwx is for user, second rwx for group, third r reprsent others
   
![image](https://github.com/user-attachments/assets/bdac7801-d3e6-4f7d-a629-0c8ce96ae4fa)

## 🔐 Linux File Permissions Table & Commands

This section covers how Linux file permissions work and how to manage them using common commands. File permissions are represented using binary values, which map to symbolic notations:

| Octal | User | Group | Others |
|:-----:|:----:|:-----:|:------:|
| `0`   | `-`  | `-`   | `-`    |
| `1`   | `-`  | `-`   | `x`    |
| `2`   | `-`  | `w`   | `-`    |
| `3`   | `-`  | `w`   | `x`    |
| `4`   | `r`  | `-`   | `-`    |
| `5`   | `r`  | `-`   | `x`    |
| `6`   | `r`  | `w`   | `-`    |
| `7`   | `r`  | `w`   | `x`    |

> 📘 **Legend**: `r = read`, `w = write`, `x = execute`, `- = no permission`  
> 👤 Change the ownership of a file: `sudo chown Shubham demofile.txt`  
> 👥 Change the group of a file: `sudo chgrp devops demofile.txt`  
> ✅ These permissions help control access to files and folders securely in Linux systems.

---

### ⚙️ Example Command

- 📂 **Make a folder named `cloud` readable, writable, and executable for everyone:**
  ```bash
  chmod 777 cloud

## 📦 Compression & 🔐 SCP Commands

This section helps you manage compressed files and securely transfer files between your local machine and AWS EC2 using SCP and SSH keys.

---

### 📌 Compression Commands

| Command | Description |
|--------|-------------|
| `zip -r ldf.zip linux_for_devops` | 🔄 Recursively zip the `linux_for_devops` folder into `ldf.zip`. |
| `unzip ldf.zip` | 📂 Unzip the contents of `ldf.zip`. |
| `tar -cvzf cloud.tar.gz cloud` | 📦 Create a compressed `.tar.gz` archive of the `cloud` folder.<br>🧩 `c` = create, `v` = verbose, `z` = gzip, `f` = file |
| `tar -xvzf cloud.tar.gz` | 📥 Extract the `.tar.gz` archive.<br>🔍 `x` = extract, other flags remain same. |

---

### 🔐 SCP (Secure Copy) Commands – EC2 & SSH Key


```bash
#### 🔼 Upload a file from local to EC2:
scp -i "C:\Users\Shubh\Downloads\linux-for-devops.pem" secret-file.txt ubuntu@ec2-3-80-129-116.compute-1.amazonaws.com:/home/ubuntu


  scp -i "C:\Users\Shubh\Downloads\linux-for-devops.pem" secret-file.txt ubuntu@ec2-3-80-129-116.compute-1.amazonaws.com:/home/ubuntu
    BREAKDOWN
      - scp -i  : command
      - "C:\Users\Shubh\Downloads\linux-for-devops.pem"   : private key path
      - secret-file.txt   : source
      - ubuntu@ec2-3-80-129-116.compute-1.amazonaws.com:/home/ubuntu   : destination


#### 🔼 Download a file from EC2 to local:

  scp -i "C:\Users\Shubh\Downloads\linux-for-devops.pem" -r ubuntu@ec2-3-80-129-116.compute-1.amazonaws.com:/home/ubuntu/linux_for_devops .
  here we are downloading file from server to localhost
      - added -r : for recursive copy(each)
