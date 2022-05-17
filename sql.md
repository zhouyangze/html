```powershell
mysql -h localhost -p3306 -u root -p
mysql -u root -p
show databases;
选中数据库
use [库名]
show tables;
show tables from mysql
查看当前数据库
select database();
查看结构
desc studentl;
插入数据
insert into student(id,name) values(1,'mac');
查看数据版本
mysql内:select version()
dos内：mysql --version
```



SQL

> DQL 数据查询语言

> DML 数据修改语言

> DDL 数据定义语言

> TCL  事务控制语言

![image-20220316140115335](https://picture-of-notebook.oss-cn-hangzhou.aliyuncs.com/img/image-20220316140115335.png)