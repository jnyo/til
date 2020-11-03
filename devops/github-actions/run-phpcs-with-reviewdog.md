# Run phpcs with reviewdog

1. create `phpcs.xml` on target repositry
2. add following `yml` under `.github/workflows` on targett repositry

    ```yml
    name: Lint

    on:
      pull_request: # specify a trigger to run an action
        branches:
          - 'develop' # specify PR target branch

    jobs:
      lint:
        runs-on: ubuntu-latest

        steps:
        - name: Check out Git repository
            uses: actions/checkout@v2

        - name: Setup PHP 7.3
            uses: shivammathur/setup-php@v2
            with:
            php-version: "7.3"
            coverage: none
            tools: composer

        - name: Install PHP dependencies
            run: composer global require "squizlabs/php_codesniffer=*"

        - uses: reviewdog/action-setup@v1
            with:
            reviewdog_version: latest

        - name: lint
            env:
            REVIEWDOG_GITHUB_API_TOKEN: ${{ secrets.GITHUB_TOKEN }}
            run: ~/.composer/vendor/bin/phpcs --report=emacs --standard=phpcs.xml ./ | reviewdog -reporter=github-pr-review -efm='%f:%l:%c:%m'
    ```

3. create PR and select `develop` branch as target
