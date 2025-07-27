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

## 📸 AWS EBS Snapshots

### 💡 What is it?

- A **snapshot** is like taking a **photo of your hard drive** (EBS volume) at a moment in time.
- It saves your data so you can **restore it later** if something goes wrong.
- Stored by AWS securely in the background.

---

### 🔧 Why Use It?

- 🛑 **Backup** your data before deleting or changing anything.
- 🔁 **Restore** the same data anytime by creating a new volume from the snapshot.
- 💸 **Saves money** – only the changes after the first snapshot are stored.
- 🌍 Can copy to other AWS regions for safety.

---

### 🛠️ When to Use?

- Before stopping or terminating your EC2 instance.
- Before installing new software or updates.
- If you want to **move your data to another region**.
- To **automate backups** regularly.

---

### 🧪 Simple AWS CLI Commands

```bash
# Take a snapshot of your EBS volume
aws ec2 create-snapshot --volume-id vol-xxxxxx --description "My backup"

# List your snapshots
aws ec2 describe-snapshots --owner-ids self

# Restore a volume from your snapshot
aws ec2 create-volume --snapshot-id snap-xxxxxx --availability-zone us-east-1a

