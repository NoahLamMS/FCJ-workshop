---
title: "1.2 Cấu hình thông tin AWS"
weight: 1
draft: false
---

## 1. Tạo IAM user
- Vào AWS Console → IAM → Users → Add User.
- Bật "Programmatic access".
- Gán quyền phù hợp (ví dụ: AdministratorAccess).

## 2. Lấy Access Keys
Tải file `.csv` chứa Access Key ID và Secret Access Key.

## 3. Cấu hình trên máy tính
```bash
aws configure
# AWS Access Key ID: <mã-key-của-bạn>
# AWS Secret Access Key: <mã-secret-của-bạn>
# Default region name: ap-southeast-1
# Default output format: json
```

## 4. Kiểm tra cấu hình
```bash
aws s3 ls
```
