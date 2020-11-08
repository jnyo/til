# backup and restore

## create dump

```sh
mysqldump -u [USER_NAME] -p [DATABASE_NAME] > dump.sql
```

## restore from dump

```sh
mysql -u [USER_NAME] -p [DATABASE_NAME] < dump.sql
```
