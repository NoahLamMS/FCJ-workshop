---
title: "1.2 Configure AWS Credentials"
weight: 1
draft: false
---

## 1. Create an IAM user
- Go to AWS Console → IAM → Users → Add User.
- Enable "Programmatic access".
- Assign appropriate permissions (e.g., AdministratorAccess).

## 2. Get Access Keys
Download `.csv` file containing Access Key ID and Secret Access Key.

## 3. Configure locally
```bash
aws configure
# AWS Access Key ID: <your-key-id>
# AWS Secret Access Key: <your-secret-key>
# Default region name: ap-southeast-1
# Default output format: json
```

## 4. Test configuration
```bash
aws s3 ls
```
