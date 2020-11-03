# Remove a tapped formula repository

1. lists the currently tapped repositories - `tap` without arguments.

    ```zsh
    ❯ brew tap
    aoki/redis-cli
    homebrew/cask
    homebrew/core
    ringohub/redis-cli # target to be removed
    ```

2. Remove a tapped formula repository - `untap`

    ```zsh
    ❯ brew untap ringohub/redis-cli
    Untapping ringohub/redis-cli...
    Untapped 1 formula (75 files, 41.9KB).
    ```
