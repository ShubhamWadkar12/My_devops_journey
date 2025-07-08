##  🖥️  Linux Architecture

<img src="https://github.com/user-attachments/assets/3bc7cf1e-7540-4eda-8b5a-2a39086eaf9f" alt="Image" width="300"/>

- Application -> Shell -> Kernel -> Hardware
- E.g. To create a new folder

---

## What is Bootloader?
- A **bootloader** is a small program that starts your operating system when you turn on your computer or device.
- E.g. GRUB (GRand Unified Bootloader)

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

