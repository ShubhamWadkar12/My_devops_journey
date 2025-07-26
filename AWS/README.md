# ☁️ **Cloud Computing Overview**

**What is cloud computing?**
> delivering computing services over the internet instead of using local servers or personal devices. Cloud = Using someone else's computer (like AWS, Azure, Google Cloud) over the internet to store data, run applications, or access services.

**What cloud includes?**
> - Storage – Like Google Drive or Dropbox (store files online)
> - Servers – Run websites or apps (e.g., hosting a website on AWS EC2)
> - Databases – Cloud-based databases like Amazon RDS or Firebase
> - Networking – Secure communication and load balancing
> - Software as a Service (SaaS) – Using apps via browser (e.g., Gmail, Zoom)
> - Platform as a Service (PaaS) – Developers build apps without managing servers
> - Infrastructure as a Service (IaaS) – Full control over cloud servers and storage
✅ **Why Cloud is Popular in IT?**
> - Scalable – Add or remove resources anytime
> - Cost-effective – Pay only for what you use
> - Accessible – Work from anywhere
> - Reliable – High uptime with backups
> - Secure – Advanced security tools and encryption
---
### 🤜🤛 Public Cloud vs Private Cloud

| 🔍 **Point**      | 🌐 **Public Cloud**                       | 🏢 **Private Cloud**                               |
| ----------------- | ----------------------------------------- | -------------------------------------------------- |
| **Who owns it?**  | Big companies like AWS, Google, Microsoft | Your company or a private vendor                   |
| **Who uses it?**  | Anyone can use it (shared with others)    | Only your company uses it                          |
| **Cost**          | Cheaper (pay only for what you use)       | More expensive (you set it up and maintain it)     |
| **Security**      | Good, but shared with others              | Very secure (only you use it)                      |
| **Speed & Scale** | Very fast and can grow easily             | Not as fast to grow – needs planning               |
| **Control**       | Less control (provider manages it)        | Full control (you manage everything)               |
| **Use Case**      | Good for websites, apps, small companies  | Good for banks, hospitals, government use          |
| **Example**       | Using Google Drive or hosting on AWS      | A bank's private system inside its own data center |

**Why public cloud is used widely?**
> - ✅ Easy to start – Just sign up and use.
> - 💰 Low cost – Pay only for what you use.
> - 🛠️ No setup needed – No need to buy or manage servers.
> - ⚡ Quick access – Services ready in minutes.
> - 🌍 Accessible anywhere – Use from any device, any location.
> - 📈 Scalable – Can grow as your needs grow.
> - 🔒 Reliable – Built-in security and backups.
> - 🧪 Free trials available – Try before you pay.
> - 👨‍💻 Good for all – Students, startups, big companies.
> - 🧰 Many services – Storage, hosting, AI, databases, and more.

**Why is AWS the leading cloud provider in todays market?**
> - 🌍 First Mover Advantage – AWS started early in 2006, before others.
> - 🏢 Backed by Amazon – Trusted and funded by a tech giant.
> - 🔧 Huge Service Range – Offers 200+ services (compute, storage, AI, etc.).
> - 📍 Global Reach – Data centers in many countries (called regions & zones).
> - 💪 Highly Reliable – Strong uptime and backups.
> - 📈 Scales Easily – Used by Netflix, NASA, Airbnb, and startups alike.
> - 🔒 Strong Security – Enterprise-grade security features and compliance.
> - 💼 Enterprise Friendly – Designed to handle massive business needs.
> - 🧪 Innovation Leader – Keeps adding new tools like AI, ML, and serverless.
> - 🧰 Developer Tools – Great support for DevOps, automation, and CI/CD.
> - 💰 Flexible Pricing – Pay-as-you-go + free tier for beginners.
> - 📚 Lots of Learning Resources – Courses, certifications, and community.

### **🔐 AWS IAM**
> - IAM stands for Identity and Access Management.
> - It is a security service in AWS that helps you control who can do what in your AWS account.
> - AWS IAM lets you create users, give them passwords or keys, and control what they can access in your AWS account.
> - For example, instead of giving everyone the same admin login (which is risky), you can create separate IAM users for your teammates and give them only the permissions they need nothing more. This is called the principle of least privilege, and it helps reduce mistakes and improve security.
> - You can also create IAM roles for your automation tools like Jenkins or Terraform. These roles allow your tools to access services like S3 or EC2 without using passwords they use secure tokens instead. That way, your pipelines can run smoothly and safely without manual login or exposing secret keys.
> - Another great benefit is that IAM works with CloudTrail, so you can track who did what in your AWS account. This is very helpful for auditing, debugging, or just knowing if something goes wrong.
> - IAM also supports Multi-Factor Authentication (MFA), so you can protect important accounts with a second layer of security (like a phone code), which is especially important for production environments.

### Authentication and Authorisation
> - **Authentication** is about proving your identity, A username and password.
> - AWS checks: "Is this person allowed to enter the AWS account?"
> - **Authorization** is about what actions you're allowed to perform.
> - Once you're logged in (authenticated), IAM checks your permissions (policies).
