# Lessons Learned

## Overview

This project helped me understand how Identity and Access Management (IAM) works in Google Cloud and why it is one of the most important parts of cloud security.

By working with different users, roles, service accounts, and virtual machines, I learned how organizations control access to cloud resources and protect their infrastructure from unauthorized actions.

---

## What I Learned

### Understanding IAM

I learned that IAM is responsible for controlling who can access cloud resources and what actions they can perform. Every user or service account must have the correct permissions before interacting with resources.

---

### Importance of Least Privilege

One of the biggest lessons from this project was the Principle of Least Privilege.

When User 2 had only the Viewer role, creating a virtual machine failed because the required permissions were missing. This showed how cloud environments prevent unauthorized changes by restricting access based on roles.

---

### Role-Based Access Control (RBAC)

Instead of assigning permissions one by one, Google Cloud groups permissions into roles.

I learned how predefined roles such as Owner and Viewer work, and how they simplify access management across projects.

---

### Creating Custom Roles

I created a custom DevOps role with specific permissions required to manage virtual machines.

This helped me understand how organizations can provide only the permissions needed for a particular job without granting full administrative access.

---

### Service Accounts

I learned how service accounts act as machine identities and allow applications or virtual machines to perform tasks securely without using personal user credentials.

This is an important concept for automation and cloud operations.

---

### Testing and Validation

I tested both successful and failed access scenarios.

Seeing permission-denied errors and then fixing them through proper IAM configuration helped me understand how access control works in real cloud environments.

---

### Real-World Cloud Security

This project showed me how cloud administrators and security engineers manage users, permissions, and resources in enterprise environments.

It was my first hands-on experience implementing cloud security controls instead of just reading about them.

---

## Skills Developed

* Google Cloud IAM
* Role-Based Access Control (RBAC)
* Service Account Management
* Compute Engine Administration
* Access Control
* Cloud Security Fundamentals
* Google Cloud CLI (gcloud)
* Security Documentation

---

## Conclusion

Through this project, I gained practical experience in managing cloud identities, assigning permissions, creating custom roles, and securing cloud resources.

More importantly, I learned how proper access control helps protect cloud environments and how IAM plays a critical role in modern cloud security.
