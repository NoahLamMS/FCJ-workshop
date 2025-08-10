---
title: "1.3 Bootstrap AWS CDK"
weight: 1
draft: false
---


Bootstrapping prepares your AWS environment for AWS CDK deployment.

```bash
cdk bootstrap aws://<account-id>/<region>
```

Example:
```bash
cdk bootstrap aws://123456789012/ap-southeast-1
```

This creates necessary resources (e.g., S3 buckets, roles) for deployment.
