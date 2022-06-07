
# 调试
## gdb
run	运行
start	开始调试
b+*地址/函数名		断点
c	继续运行
info	查看信息
d	删除
ni	步过
si	步入
x/查看内存     
>+s(字符串）
>+数字（字节数）+进制（x为十六进制）+单位（b为byte（1字节），w为word（4），g（8））
## idapro cheatsheet（略，用时自己找去）
- F5	反编译
- tab	在视图和代码之间转换****** 空格是带地址的 *******
- r	转字符
- h	转十六进制数字
- n	重命名
- **_	按补码解析为负数
- ~	按位取反
- esc	上一步
- ctrl+enter	下一步
- alt+b	搜索字节数据
- alt+t	找地址
- alt+k	修改值
- alt+f7	执行脚本
- f2	十六进制窗口修改数据，再次按应用修改
- shift+f12	打开字符串窗口

- delete	删除函数
- p	定义函数
- 窗口 ctrl+e 或 反汇编窗口 alt+p	修改函数参数函数

- ctrl+s	跳转到某一区段
- g	跳转到已定义的名称/地址

- 
lazyida:
- w	复制地址
- shift+G	跳转到剪切板中的地址
keypatch:
- ctrl+alt+k	修改命令






 



