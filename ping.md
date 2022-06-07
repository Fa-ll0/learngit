1. 检查网络问题的步骤
- ping 127.0.0.1	检查基础配置是否正常，tcpip是否正常安装
- ping 本机地址（内网ip）/localhost(hosts中不解析为127.0.0.1时）	检查网线和wifi链接
- ping 路由器192.168.10.1	检查路由器
- ping 目标ip
- ping 域名
2. 关于用法
- windows发送4条请求，linux和macos无限发送，ctrl+c停止
- 规定请求次数:  ping -c 次数 ip地址
- -a 成功发出声音 -i(s) 设置发送时间间隔 -q 不显示
3. 死ping ping -l 65532 ip

