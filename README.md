**New: [wireguard-install](https://github.com/Nyr/wireguard-install) is also available.**

## openvpn-install
OpenVPN [road warrior](http://en.wikipedia.org/wiki/Road_warrior_%28computing%29) installer for Ubuntu, Debian, AlmaLinux, Rocky Linux, CentOS and Fedora.

This script will let you set up your own VPN server in no more than a minute, even if you haven't used OpenVPN before. It has been designed to be as unobtrusive and universal as possible.

### Installation
Run the script and follow the assistant:

`wget https://git.io/vpn -O openvpn-install.sh && bash openvpn-install.sh`

Once it ends, you can run it again to add more users, remove some of them or even completely uninstall OpenVPN.

### I want to run my own VPN but don't have a server for that
You can get a VPS from just 2€/month at [AlphaVPS](https://alphavps.com/clients/aff.php?aff=474&pid=422).

### Donations

If you want to show your appreciation, you can donate via [PayPal](https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=VBAYDL34Z7J6L) or [cryptocurrency](https://pastebin.com/raw/M2JJpQpC). Thanks!
一键部署超级简单易用的openvpn服务器，支持多证书+多账号[密码]认证

一. 服务器端部署
项目地址：GitHub - guoew/openvpn-install: OpenVPN road warrior installer for Debian, Ubuntu and CentOS

1.1. 下载安装
git clone https://github.com/guoew/openvpn-install.git
cd openvpn-install &&  bash openvpn-install.sh
然后按步骤操作 

Welcome to this OpenVPN "road warrior" installer!
 
I need to ask you a few questions before starting the setup.
You can leave the default options and just press enter if you are ok with them.
 
First, provide the IPv4 address of the network interface you want OpenVPN              
listening to. 
IP address: 172.28.0.3               ----直接回车
 
This server is behind NAT. What is the public IPv4 address or hostname?
Public IP address / hostname: xxx.xxx.xxx.xxx 外网ip
 
Which protocol do you want for OpenVPN connections?
   1) UDP (recommended)
   2) TCP
Protocol [1-2]: 1
 
What port do you want OpenVPN listening to?
Port: 5556
 
Which DNS do you want to use with the VPN?
   1) Current system resolvers
   2) 1.1.1.1
   3) Google
   4) OpenDNS
   5) Verisign
DNS [1-5]: 1
 
Finally, tell me your name for the client certificate.
Please, use one word only, no special characters.
Client name: yangzhou         --创建vpn用户，默认client，可以直接回车，自行选择
 
Okay, that was all I needed. We are ready to set up your OpenVPN server now.
Press any key to continue...
已加载插件：fastestmirror, langpacks
Repository epel is listed more than once in the configuration
Repository epel is listed more than once in the configuration
Repository epel-debuginfo is listed more than once in the configuration
Repository epel-source is listed more than once in the configuration
Loading mirror speeds from cached hostfile
 * centos-sclo-rh: mirror.fra10.de.leaseweb.net
软件包 epel-release-7-14.noarch 已安装并且是最新版本
无须任何处理
已加载插件：fastestmirror, langpacks
Repository epel is listed more than once in the configuration
Repository epel is listed more than once in the configuration
Repository epel-debuginfo is listed more than once in the configuration
Repository epel-source is listed more than once in the configuration
Loading mirror speeds from cached hostfile
 * centos-sclo-rh: mirror.fra10.de.leaseweb.net
软件包 iptables-1.4.21-35.el7.x86_64 已安装并且是最新版本
软件包 1:openssl-1.0.2k-21.el7_9.x86_64 已安装并且是最新版本
软件包 ca-certificates-2021.2.50-72.el7_9.noarch 已安装并且是最新版本
正在解决依赖关系
--> 正在检查事务
---> 软件包 openvpn.x86_64.0.2.4.11-1.el7 将被 安装
--> 解决依赖关系完成
 
依赖关系解决
 
================================================================================================================================================================================================================================================================
 Package                                                       架构                                                         版本                                                               源                                                          大小
================================================================================================================================================================================================================================================================
正在安装:
 openvpn                                                       x86_64                                                       2.4.11-1.el7                                                       epel                                                       527 k
 
事务概要
================================================================================================================================================================================================================================================================
安装  1 软件包
 
总下载量：527 k
安装大小：1.2 M
Downloading packages:
openvpn-2.4.11-1.el7.x86_64.rpm                                                                                                                                                                                                          | 527 kB  00:00:02     
Running transaction check
Running transaction test
Transaction test succeeded
Running transaction
  正在安装    : openvpn-2.4.11-1.el7.x86_64                                                                                                                                                                                                                 1/1 
  验证中      : openvpn-2.4.11-1.el7.x86_64                                                                                                                                                                                                                 1/1 
 
已安装:
  openvpn.x86_64 0:2.4.11-1.el7                                                                                                                                                                                                                                 
 
完毕！
 
init-pki complete; you may now create a CA or requests.
Your newly created PKI dir is: /etc/openvpn/server/easy-rsa/pki
 
 
Using SSL: openssl OpenSSL 1.0.2k-fips  26 Jan 2017
Generating RSA private key, 2048 bit long modulus
..............................+++
..+++
e is 65537 (0x10001)
 
Using SSL: openssl OpenSSL 1.0.2k-fips  26 Jan 2017
Generating a 2048 bit RSA private key
........................................+++
.....................................................................................+++
writing new private key to '/etc/openvpn/server/easy-rsa/pki/easy-rsa-7646.2pG6Rk/tmp.hxnW4c'
-----
Using configuration from /etc/openvpn/server/easy-rsa/pki/easy-rsa-7646.2pG6Rk/tmp.twLmR0
Check that the request matches the signature
Signature ok
The Subject's Distinguished Name is as follows
commonName            :ASN.1 12:'server'
Certificate is to be certified until Oct 12 07:29:27 2031 GMT (3650 days)
Write out database with 1 new entries
Data Base Updated
Using SSL: openssl OpenSSL 1.0.2k-fips  26 Jan 2017
Generating a 2048 bit RSA private key
.........................................................................................................+++
.............+++
writing new private key to '/etc/openvpn/server/easy-rsa/pki/easy-rsa-7738.fLRMAQ/tmp.uEwI2e'
-----
Using configuration from /etc/openvpn/server/easy-rsa/pki/easy-rsa-7738.fLRMAQ/tmp.zb5J81
Check that the request matches the signature
Signature ok
The Subject's Distinguished Name is as follows
commonName            :ASN.1 12:'yangzhou'                            
Certificate is to be certified until Oct 12 07:29:27 2031 GMT (3650 days)
 
Write out database with 1 new entries
Data Base Updated
 
Using SSL: openssl OpenSSL 1.0.2k-fips  26 Jan 2017
Using configuration from /etc/openvpn/server/easy-rsa/pki/easy-rsa-7805.u82YJj/tmp.GtEwWf
 
An updated CRL has been created.
CRL file: /etc/openvpn/server/easy-rsa/pki/crl.pem
 
 
chown: 无效的用户: "nobody.nogroup"
23423
success
success
success
success
success
success
Created symlink from /etc/systemd/system/multi-user.target.wants/openvpn-server@server.service to /usr/lib/systemd/system/openvpn-server@.service.
 
Finished!
 
Your client configuration is available at: /root/yangzhou.ovpn
If you want to add more clients, you simply need to run this script again!
将客户端配置文件 /root/client.ovpn，下载到本地以备客户端使用

1.2. 添加账号
在openvpn目录下的userfile.sh中添加用户和密码，以空格隔开

cat /etc/openvpn/userfile.sh
username password
 开发云服务器端口 端口有tcp和udp 记得要开对应的

二. 客户端部署使用
2.1. 安装openvpn客户端
客户端下载地址：https://swupdate.openvpn.org/community/releases/openvpn-install-2.4.0-I602.exe
安装步骤略(可自定义安装路径)
2.2. 配置客户端
将安装好的客户端打开，点击Import file 把准备好的客户端配置文件导入进去。

2.3. 连接openvpn服务器
打开客户端，点击Connect，使用服务器端已添加的账号登录

END

附：
安装完毕后，再次执行脚本openvpn-install.sh 会有四个菜单选项(添加、撤销、卸载、退出)，可根据自身实际情况应用,如下：

Looks like OpenVPN is already installed.
 
What do you want to do?
   1) Add a new user
   2) Revoke an existing user
   3) Remove OpenVPN
   4) Exit
Select an option [1-4]:
这里有个不足之处是，当使用多证书时，账号是通用的。即同一个账号，可以应用于不同的证书。

如果想要不同用户使用不同的证书进行登录[无账号]，欢迎访问原项目地址：
https://github.com/Nyr/openvpn-install
