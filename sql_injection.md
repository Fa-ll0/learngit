# sql
（#为注释）
1.查询语句（select后*表示所有，where后1代表所有，0代表没有）
SELECT 列名 FROM 表名；
SELECT 列名 FROM 表名 WHERE 列 运算符 值；
SELECT 列名 FROM 表名 ORDER BY 列名/列序号；（按某列排序）
SELECT... （此处可换行）UNION SELECT...；(联合查询，两个拼一起构成一个新表）
2.修改语句
UPDATE
3.删除语句
DELETE
4.插入语句
INSER INFO
注入
（学长说的fuzz还不知道是什么qwq）
1.数值注入
监测方法：注入点1.后面加'看是否报错2.加and 1=1和and 1=2看是否执行
利用方法：试order by判断总列数（看是否报错）
                   联合查询如id=0 union select 1,2,3...确定显示位置
                   构造id=0 union select 1,database(),version()...确定版本信息
                   


