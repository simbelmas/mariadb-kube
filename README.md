# mariadb-kube

need ReadWriteMany storage to run binlog purge cronjob

## Bootstrap

### Binlog rotation user creation

~~~
GRANT BINLOG ADMIN on *.* TO '{BINLOG USER}'@'%' IDENTIFIED BY '{BINLOG USER PASSWORD}';
flush privileges;
~~~