# AWS

- Reminder that frankfurt is not working for s3 access for whatever reason. USE DUBLIN!!!!
- Permission for making an s3 bucket public:

```
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "Statement1",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::BUCKET_NAME/*"
    }
  ]
}
```

## Links
