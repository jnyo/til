# Configure Iam Policy for Session Manager user

- restrict access to a specific instance
- restrict access by IP
- enforce a session document check(SSH) for AWS CLI

```json
{
    "Version": "2012-10-17",
    "Statement": [
        {
            "Effect": "Allow",
            "Action": "ssm:StartSession",
            "Resource": [
                "arn:aws:ec2:*:*:instance/{instanceId}",
                "arn:aws:ssm:region:account-id:document/AWS-StartSSHSession"
            ],
            "Condition": {
                "IpAddress": {
                    "aws:SourceIp": [
                        "xxx.xxx.xxx.xxx/32"
                    ]
                },
                "BoolIfExists": {
                    "ssm:SessionDocumentAccessCheck": "true"
                }
            }
        }
    ]
}
```
