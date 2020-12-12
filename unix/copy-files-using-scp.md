# Copy files using scp

## Copy a remote file to local

```sh
scp USER_NAME@REMOTE_HOST:/REMOTE/PATH/TO/FILE /LOCAL/DIRECTOPRY
```

## Copy a local file to remote

```sh
scp /LOCAL/PATH/TO/FILE USER_NAME@REMOTE_HOST:/REMOTE/DIRECTOPRY

# use -r option to copy a directory
scp -r /LOCAL/DIRECTORY USER_NAME@REMOTE_HOST:/REMOTE/DIRECTOPRY
```
