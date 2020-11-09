# Change a remote url

1. List existing remotes

    ```sh
    $ git remote -v
    > origin  git@github.com:USERNAME/REPOSITORY.git (fetch)
    > origin  git@github.com:USERNAME/REPOSITORY.git (push)
    ```

2. Change a remote url with `set-url`

    ```sh
    $ git remote set-url origin git@github.com:NEW_USERNAME/NEW_REPOSITORY.git
    # ssh to https
    $ git remote set-url origin https://github.com/NEW_USERNAME/NEW_REPOSITORY.git
    ```
