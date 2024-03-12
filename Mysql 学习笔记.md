# Mysql 学习笔记 #

## 选择语句 ##
- sql语句不分大小写，行文规则最好大写关键字。
  ``  SELECT  * FROM students WHERE sexy='男' ORDER BY first_name;  ``
  
- --等于java中的//（注释）

- *表示all，返回所有列，但是不适用于大型表，会给服务器造成负担
  ``  SELECT  id, adress FROM students WHERE sexy='男' ORDER BY first_name;  ``
  
- SELECT 也可以查询简单表达式，如

- ``  SELECT grade+10 FROM students WHERE subject='Math' ORDER BY first_name;  ``

- as 可以给我们的查询的列一个别名，如

- ``  SELECT grade+10 AS new_grade  FROM students WHERE subject='Math' ORDER BY first_name;  ``

- where

- 逻辑运算符 > >= < <= = !=

- Mysql默认的日期表达形式 `'1999-01-01'`

- &&(AND) ||(OR)

- WHERE NOT 条件的否命题

- IN函数

  `` WHERE state = 'VA' OR state = 'GA' OR state = 'FL' ``

  等同于

  `` WHERE state IN ('VA','GA','FL') ``

- NOT 函数 

  比如`` NOT WHERE ``  和 `` NOT IN `` （否）

- BETWEEN运算符

  `` WHERE points >= 1000 AND points <= 3000 ``

  等同于

  `` WHERE points BETWEEN 1000 AND 3000``

- LIKE运算符

  LIKE '%a%'，%表示任何字符数

  LIKE '__y_', _表示一个字符数

- REGEXP 正则表达式
- 有点像`` WHERE last_name like '%field%' ``
  ^在前表示必须在前，$在尾表示必须在尾,|表示或，[a-b]表示a到b的任意字母
  `` WHERE last_name REGEXP 'field|mac|rose' ``
  `` WHERE last_name REGEXP 'field|mac|rose' ``
  `` WHERE last_name REGEXP '[ab-g]z' ``

- NULL || NOT NULL
  `` WHERE phone IS NOT NULL ``

- ORDER BY 排序
DESC 从大到小

