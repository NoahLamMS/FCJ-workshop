---
title: "2.1 Tạo dự án AWS CDK mới"
weight: 1
draft: false
---

```bash
mkdir my-cdk-app
cd my-cdk-app
cdk init app --language typescript
```

Lệnh này sẽ tạo ra:
- `bin/` → entry point
- `lib/` → mã nguồn stack chính
- `cdk.json` → cấu hình
- `package.json` → các phụ thuộc
