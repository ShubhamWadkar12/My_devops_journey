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
