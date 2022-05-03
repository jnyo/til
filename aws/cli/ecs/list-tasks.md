# List tasks

```sh
aws ecs list-tasks \
  --cluster <value> \
  --service <value> \
  --profile <value> \
  --region <value>
```

Output

```json
{
    "taskArns": [
        "arn:aws:ecs:<REGION>:<AWS_ACCOUNT_ID>:task/<ECS_CLUSTER_NAME>/<TASK_ID>"
    ]
}
```
