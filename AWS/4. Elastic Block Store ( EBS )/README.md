# 💾 AWS EBS (Elastic Block Store)

## 📘 What is EBS?

- **Amazon Elastic Block Store (EBS)** provides **persistent block storage** for Amazon EC2 instances.
- Think of it as a **hard drive attached to your EC2 instance**.
- It stores **data permanently** (even if the instance stops or restarts).

---

## ⚙️ How it Works

- You **create an EBS volume** and **attach it to an EC2 instance**.
- The instance can **read/write data** to this volume just like a local disk.
- EBS volumes can also be **detached** and **re-attached** to another instance.

---

## 📦 Types of EBS Volumes

| Volume Type        | Use Case                                  | Key Feature                     |
|--------------------|--------------------------------------------|----------------------------------|
| gp3 (General Purpose SSD) | Balanced performance and cost          | Default choice for most workloads |
| io2/io1 (Provisioned IOPS SSD) | High-performance apps (databases) | High IOPS and durability          |
| st1 (Throughput Optimized HDD) | Big data, data warehouses          | High throughput, low cost        |
| sc1 (Cold HDD)     | Infrequent access (archival)              | Very low cost                    |

---

## 🔐 EBS Features

- **Durability**: Automatically replicated within its Availability Zone.
- **Snapshots**: You can back up EBS volumes to **Amazon S3** using **snapshots**.
- **Encryption**: Supports encryption at rest and in transit.
- **Scalability**: You can resize volumes without downtime.

---

## 🚀 Common Use Cases

- Running databases like MySQL, PostgreSQL, MongoDB
- Hosting file systems or media content
- Boot volumes for EC2 instances
- Backup and restore using Snapshots

---

📌 *Tip: Always monitor EBS performance and use the right volume type for your workload to optimize cost and efficiency.*
