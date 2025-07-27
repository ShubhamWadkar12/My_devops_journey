## 🔐 AWS IAM (Identity and Access Management)

IAM (Identity and Access Management) is an AWS security service that helps you **control access** to AWS resources by defining **who can do what** in your account.

---

### 📘 What is AWS IAM?

> - IAM lets you **create users**, assign **passwords or access keys**, and define **permissions**.
> - It helps follow the **principle of least privilege** users only get access to what they need.
> - Instead of sharing one admin login (a big security risk!), create **individual IAM users** for each teammate.
> - IAM works with **automation tools** like **Jenkins** or **Terraform** using secure **IAM Roles**, not passwords.
> - It integrates with **AWS CloudTrail** for **activity tracking, auditing, and debugging**.
> - Supports **Multi-Factor Authentication (MFA)** for stronger protection essential in **production environments**.

---

### 🔑 Authentication vs Authorization

| Term             | Meaning                                                                 |
|------------------|-------------------------------------------------------------------------|
| **Authentication** | 🔐 Verifying identity (e.g., login with username and password)            |
| **Authorization**  | ✅ Determining what actions the user is allowed to perform (via policies) |

> - **Authentication**: "Is this user really who they say they are?"
> - **Authorization**: "What is this user allowed to do after logging in?"

---

# 🔐 AWS IAM Best Practices

Follow these best practices to secure your AWS Identity and Access Management (IAM):

---

- ✅ **Avoid using the root account** except for the initial account setup.
- 👥 **Add users to groups** and assign permissions to the **group**, not the individual.
- 🔒 **Use strong password policies** and enable **MFA (Multi-Factor Authentication)**.
- 🔑 **Use Access Keys** only for **CLI or SDK** usage never for web console login.
- 🚫 **Never share Access Keys or passwords** with anyone.
- 📊 **Audit permissions regularly** using the **IAM Credential Report**.

---

> ✅ Tip: Always apply the principle of least privilege give only the permissions a user really needs.
