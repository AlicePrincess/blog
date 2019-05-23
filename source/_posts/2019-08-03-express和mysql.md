---
layout: post
title: 'express集成mysql'
subtitle: '将数据库的数据进行读写'
date: 2018-08-03
categories: 技术
cover: 'http://pcvfuus6c.bkt.clouddn.com/cover/blog_4.jpg'
tags: 技术 express mysql
---
## 介绍mysql
MySQL是一个关系型数据库管理系统，由瑞典MySQL AB 公司开发，目前属于 Oracle 旗下产品。MySQL 是最流行的关系型数据库管理系统之一，在 WEB 应用方面，MySQL是最好的 RDBMS (Relational Database Management System，关系数据库管理系统) 应用软件。

## 安装mysql模块

```bash
$ npm install mysql
```
## 集成mysql

```javascript
var mysql      = require('mysql');
var connection = mysql.createConnection({
  host     : 'localhost',
  user     : 'dbuser',
  password : '123456'
});

connection.connect();

connection.query('SELECT 1 + 1 AS solution', function(err, rows, fields) {
  if (err) throw err;
  console.log('The solution is: ', rows[0].solution);
});

connection.end();
```