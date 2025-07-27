# 💾 AWS EBS (Elastic Block Store)

## ✅ What is EBS?

- EBS is like a **hard drive for your EC2 instance**.
- It stores your **files, data, and software**.
- Even if your EC2 instance stops or restarts, your data stays safe.

---

## ⚙️ How It Works

1. You **create** an EBS volume.
2. You **attach** it to your EC2 instance.
3. Your instance can **read and write** data to it like a normal disk.
4. You can also **detach** and use it with another EC2.
5. You can also Modify the size after creating the volume

---

## 📦 Types of EBS Volumes

| Type      | Best For                        |
|-----------|----------------------------------|
| gp3       | General use (default)           |
| io2/io1   | High-speed apps like databases  |
| st1       | Big data and streaming files    |
| sc1       | Backup and rarely used data     |

---

## 🔐 Features of EBS

- **Keeps data safe** in one region (AZ).
- You can take **backups (snapshots)**.
- You can **encrypt** the data.
- You can **increase size** anytime.

---

## 🚀 When to Use

- Hosting a **website or app**
- Saving **databases**
- Creating **backup copies**
- Running **software** that needs storage

---

💡 *Use the right EBS type to save money and get better performance.*
