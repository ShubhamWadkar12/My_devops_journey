## 🧊 What is AWS AMI?

**Amazon Machine Image (AMI)** is a template used to create virtual servers (EC2 instances) in AWS.

An AMI includes:
- An operating system (like Ubuntu or Windows)
- Pre-installed software and libraries
- Configuration settings

### 🔧 Why Use AMI?

- Quickly launch servers with the same setup
- Save time no need to reinstall everything
- Helps with backups, scaling, and consistency

### 🧠 Example

1. Set up an EC2 instance with your app and tools
2. Create an AMI from that instance
3. Launch more EC2 instances using that AMI

This ensures all your servers have the exact same configuration.

## 📸 How to Create an AMI from an Existing EC2 Instance

You can create a reusable image (AMI) from your current EC2 instance. Here's how:

### 🪜 Steps:

1. **Go to EC2 Dashboard** in AWS Console.
2. In the left menu, click on **Instances**.
3. Find and **select your running instance**.
4. Click **Actions → Image and templates → Create Image**.
5. Enter:
   - **Image Name** (any name you like)
   - Optional: Add a description
   - Choose whether to **reboot the instance** (recommended for a clean image)
6. Click **Create Image**.

### 🕒 What Happens Next?

- Your AMI will be created and visible under:
  - **EC2 Dashboard → Images → AMIs**
- Once ready, you can launch new EC2 instances from it.

### 💡 Tip:

Use custom AMIs to:
- Quickly spin up new servers with the same setup
- Maintain consistent environments
- Easily recover from failures

