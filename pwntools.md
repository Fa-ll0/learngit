

# pwntools
## `from pwn import *`
- `c=remote("domain/ip",port)`返回一个对象
1. 属性：
-   ***`send(payload)`  发送payload
-   ***`sendline(payload)`  发送payload，并进行换行（末尾**\n**）
-   ***`sendafter(some_string, payload)`  接收到 some_string 后, 发送你的 payload
-   `recvn(N)`  接受 N(数字) 字符
-   `recvline()`  接收一行输出
-   `recvlines(N)`  接收 N(数字) 行输出
-   ***`recvuntil(some_string)`  接收到 some_string 为止
> `p32()` 可以让我们转换整数到小端序格式. `p32` 转换4字节. `p64` 和 `p16` 则分别转换 8 bit 和 2 bit 数字. 
> `c.sendline` 将我们的payload发送到远程主机.
> `c.interactive()` 允许我们在终端里将命令传送到远程服务器. Pwntools 会自动接收输出并回显
2. 后面的东西太多了，暂时不想看啦，反正桥到船头自然直


