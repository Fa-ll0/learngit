1. 方法：（控制参数）rop（ret oriented promgramming）使用gadget（以ret为结尾的指令），注意平衡
                （无法覆盖ret）stack pivoting（栈迁移）
3. 保护机制：
- relro(aslr)     地址随机化
- nx(dep)        数据执行防护
- canary(fs)    栈溢出保护
- pie               代码地址随机化
4. 类型：
ret2text  
ret2shellcode
