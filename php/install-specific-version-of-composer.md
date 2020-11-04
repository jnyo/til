# Install a specific version of composer

Background:
Composer released v2.0 on 2020/10/24. Now w/o specifing version, installer will download v2.0.

```sh
# composer
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');" && \
php -r "if (hash_file('sha384', 'composer-setup.php') === 'c31c1e292ad7be5f49291169c0ac8f683499edddcfd4e42232982d0fd193004208a58ff6f353fde0012d35fdd72bc394') { echo 'Installer verified'; } else { echo 'Installer corrupt'; unlink('composer-setup.php'); } echo PHP_EOL;" && \
php composer-setup.php --version=1.10.17 && \
mv composer.phar /usr/local/bin/composer
```
