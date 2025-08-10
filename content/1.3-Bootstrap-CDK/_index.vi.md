---
title: "1.3 Khởi tạo môi trường AWS CDK"
weight: 1
draft: false
---

Khởi tạo môi trường giúp chuẩn bị AWS cho việc triển khai CDK.

```bash
cdk bootstrap aws://<account-id>/<region>
```

Ví dụ:
```bash
cdk bootstrap aws://123456789012/ap-southeast-1
```

Lệnh này sẽ tạo các tài nguyên cần thiết (ví dụ: S3 bucket, role) cho việc triển khai.
