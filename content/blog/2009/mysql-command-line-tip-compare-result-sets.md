---
title: "MySQL command-line tip: compare result sets"
date: "2009-03-25"
url: /blog/2009/03/25/mysql-command-line-tip-compare-result-sets/
categories:
  - Databases
  - Open Source
---
Here's a quick productivity tip: when optimizing queries by rewriting them to different forms that should return the same results, you can verify that you get the same results by taking a checksum of them.

Just set your pager to `md5sum`:

```
mysql> pager md5sum -
PAGER set to 'md5sum -'
mysql> select * from test;
a09bc56ac9aa0cbcc659c3d566c2c7e4  -
4096 rows in set (0.00 sec)
```


