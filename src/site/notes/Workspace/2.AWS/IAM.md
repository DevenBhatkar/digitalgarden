---
{"dg-publish":true,"permalink":"/workspace/2-aws/iam/","noteIcon":""}
---


## IAM (Identity and Access Management) – Introduction

**IAM (Identity and Access Management)** is the **security and access control service** in AWS. It helps you **manage who can do what** in your AWS account.

When you create an AWS account, you start with **one root user** (the owner). But you should **never use the root user for daily tasks** — instead, use IAM to create **separate users** with proper permissions.

---

### 🧑‍💻 IAM Users

An **IAM user** represents **a single person or application** that needs access to your AWS resources.

- Each user has:
    
    - A unique name
        
    - Optional **login credentials** (username + password) for the AWS Console
        
    - Optional **access keys** for programmatic access (via AWS CLI or SDK)
        
- Users can be given **permissions** directly or through groups
    

**Example**: You create an IAM user named `deven-dev` who can only access S3 buckets and nothing else.

---

### 👥 IAM Groups

An **IAM group** is a **collection of users** with the same permissions.

- Instead of assigning permissions to each user individually, you assign them to a group
    
- Users can belong to **multiple groups**
    
- Groups **do not** have login credentials — only users do
    

**Example**: You create a group called `Developers` that has permission to use EC2 and S3. Every developer you add to that group automatically gets those permissions.

---

### 🛡️ IAM Policies

A **policy** is a **set of rules** written in JSON that defines **what actions are allowed or denied**.

- Policies can be attached to:
    
    - **Users**
        
    - **Groups**
        
    - **Roles** (used for services or cross-account access)
        
- A policy defines:
    
    - **Effect**: Allow or Deny
        
    - **Action**: What actions are being allowed/denied (e.g., `s3:PutObject`)
        
    - **Resource**: Which AWS resource it applies to (e.g., a specific S3 bucket)
        

**Example Policy** (allows read-only access to S3):
```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": ["s3:GetObject"],
      "Resource": ["arn:aws:s3:::example-bucket/*"]
    }
  ]
}
```

### Summary Table

|Concept|Purpose|Example|
|---|---|---|
|**User**|Individual person or app|`john_admin`|
|**Group**|Set of users with same permissions|`AdminTeam`, `DevTeam`|
|**Policy**|JSON-based permission rules|Allow S3 read, deny EC2 launch|

---

### Best Practices

- **Don’t use the root user** for daily work
    
- **Assign least privilege** (only the permissions needed)
    
- **Use groups** to manage permissions efficiently
    
- **Rotate access keys regularly**