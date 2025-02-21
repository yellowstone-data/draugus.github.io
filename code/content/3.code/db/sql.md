---
title: SQL
icon: vscode-icons:file-type-plsql
---

<h3><a href = "https://www.runoob.com/sql/sql-insert-into-select.html" title="more info" target="_blank">SQL INSERT INTO SELECT 语法</a></h3>

* 从一个表中复制所有的列插入到另一个已存在的表中：

    ```sql
    INSERT INTO table2 SELECT * FROM table1;
    ```

* 只复制希望的列插入到另一个已存在的表中：

    ```sql
    INSERT INTO table2 (column_name(s)) SELECT column_name(s) FROM table1;
    ```

* 复制表结构及其数据：

    ```sql
    create table table_name_new as select * from table_name_old
    ```

* 只复制表结构：

    ```sql
    create table table_name_new as select * from table_name_old where 1=2;
    ```

    或者：

    ```sql
    create table table_name_new like table_name_old
    ```

* 只复制表数据：

  * 如果两个表结构一样：

    ```sql
    insert into table_name_new select * from table_name_old
    ```

  * 如果两个表结构不一样：

    ```sql
    insert into table_name_new(column1,column2...) select column1,column2... from table_name_old
    ```
