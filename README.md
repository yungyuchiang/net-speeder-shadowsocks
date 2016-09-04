# net-speeder-shadowsocks
搬瓦工VPS主机安装net-speeder加速工具

虽然我们选择便宜搬瓦工VPS从速度和使用体验上看还是对得起付出的成本的，但是如果能通过第三方工具或者VPS主机自身的优化提速可以解决我们项目的效率问题。

net-speeder工具的原理：主要通过TCP双线发包的方式，可以解决丢包问题，不过消耗的流量是双倍。

第一步：下载文件

wget http://www.banwagong.me/tools/centos_net-speeder.sh

![alt tag](https://github.com/jhx314/net-speeder-shadowsocks/blob/master/001.png)

第二步:安装

sh centos_net-speeder.sh

![alt tag](https://github.com/jhx314/net-speeder-shadowsocks/blob/master/002.png)

安装结果

![alt tag](https://github.com/jhx314/net-speeder-shadowsocks/blob/master/003.png)

第三步：运行:

nohup /usr/local/net_speeder/net_speeder venet0 "ip" >/dev/null 2>&1 &

![alt tag](https://github.com/jhx314/net-speeder-shadowsocks/blob/master/004.png)

第四步：开机启动:

echo 'nohup /usr/bin/net_speeder venet0 "ip" >/dev/null 2>&1 &' >> /etc/rc.local
