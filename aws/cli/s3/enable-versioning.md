# Enable versioning

- put bucket versioning

```sh
aws s3api put-bucket-versioning --bucket {bucket} --versioning-configuration Status=Enabled
```

- list object versions

```sh
aws s3api list-object-versions --bucket {bucket}
```
