---
title: "2.2 Định nghĩa Stack đầu tiên"
weight: 1
draft: false
---

Chỉnh sửa `lib/lambda-api-stack.ts`:


```typescript
import { LambdaWithApi } from './constructs/lambda-with-api';
import { Construct } from 'constructs';
import { Stack, StackProps } from 'aws-cdk-lib';
import * as s3 from 'aws-cdk-lib/aws-s3';

interface LambdaApiStackProps extends StackProps {
  bucket: s3.IBucket;
}

export class LambdaApiStack extends Stack {
  constructor(scope: Construct, id: string, props: LambdaApiStackProps) {
    super(scope, id, props);

    new LambdaWithApi(this, 'LambdaWithApi', {
      bucket: props.bucket,
    });
  }
}

```


```typescript
#!/usr/bin/env node
import * as cdk from 'aws-cdk-lib';
import { BucketStack } from '../lib/bucket-stack';
import { LambdaApiStack } from '../lib/lambda-api-stack';

const app = new cdk.App();

// Tạo bucket stack
const bucketStack = new BucketStack(app, 'BucketStack');

// Tạo lambda + api stack, truyền bucket từ bucketStack sang lambda
new LambdaApiStack(app, 'LambdaApiStack', {
  bucket: bucketStack.bucket,
});

```



Triển khai:
```bash
cdk deploy
```