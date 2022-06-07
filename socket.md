

#  windows利用socket

- 端口：
   www 80 
   ftp 21
   
- tcp：面向连接
数据不丢失，按顺序，不存在数据边界（接收的数据大小由接收者自己规定）
- udp：面向消息
强调快速而非顺序，数据可能丢失或损毁，限制每次传输数据的大小，传输数据有数据边界

流套接字           SOCK_STREAM             tcp，不支持广播，多播 
数据包套接字    SOCK_DGRAM             udp，支持广播，多播
原始套接字        SOCK_RAW                  读写内核未处理的ip报

基本函数
socket		         创建套接字	                                      
bind		            将套接字绑定本地ip和端口号	          	
connect	        请求连接	                                          面向连接的传输的客户机进程
listen	            侦听连接请求		                                  面向连接的传输的服务器进程		
tcp：
send，recv
udp:	
sendto,recvfrom
close				关闭套接字

数据类型
sockaddr(操作系统里的）
sockaddr_in（正常用的）
