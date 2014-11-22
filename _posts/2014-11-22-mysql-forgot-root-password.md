---
layout: post
title: MySQL忘记root密码重设
category: MySQL
date: 2014-11-22 23:42
---

以如下方式启动mysql
```bash
$ ./mysqld --skip-grant-table --user=root
```

使用mysql连接上
```bash
$ ./mysql -u root
```

执行
```sql
UPDATE mysql.user SET Password=PASSWORD('123456') where user='root';
FLUSH PRIVILEGES;
```
