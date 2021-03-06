## R2S 基于原生OpenWRT 的固件(AS IS, NO WARRANTY!!!)
![NanoPi-R2S-OpenWrt](https://github.com/vgist/NanoPi-R2S-OpenWrt/workflows/NanoPi-R2S-OpenWrt/badge.svg)

Fork 自 [QiuSimons/R2S-OpenWrt](https://github.com/QiuSimons/R2S-OpenWrt)，做了一些增减，个人自用。

### 下载地址：
https://github.com/vgist/NanoPi-R2S-OpenWrt/releases

### 本地一键编译命令（注意装好依赖）：
安装依赖：
```shell
sudo -E apt-get install -y build-essential asciidoc binutils bzip2 gawk gettext git libncurses5-dev libz-dev patch unzip zlib1g-dev lib32gcc1 libc6-dev-i386 subversion flex uglifyjs git-core gcc-multilib g++-multilib p7zip p7zip-full msmtp libssl-dev texinfo libreadline-dev libglib2.0-dev xmlto qemu-utils upx libelf-dev autoconf automake libtool autopoint ccache curl wget vim nano python python3 python-pip python3-pip python-ply python3-ply haveged lrzsz device-tree-compiler scons
```
```shell
wget -O - https://raw.githubusercontent.com/friendlyarm/build-env-on-ubuntu-bionic/master/install.sh | bash
```
一键编译（测试编译环境是Ubuntu18.04）：
```shell
git clone https://github.com/vgist/NanoPi-R2S-OpenWrt.git && cd NanoPi-R2S-OpenWrt && bash onekeyr2s.sh
```
### 注意事项：

0. OC至1.608GHz（未提升电压，原则上不会增加大量额外发热）
1. 登陆IP：192.168.2.1 密码：无
2. OP内置升级可用
3. 遇到上不了网的，请自行排查自己的ipv6联通情况。（推荐关闭ipv6）
4. 刷写或升级后遇到任何问题，可以尝试ssh进路由器，输入fuck，回车后等待重启，或可解决
5. sys灯引导时闪烁，默认启动后常亮，可以在luci菜单中设置

### 版本信息：
其他模块版本：SNAPSHOT（当日最新）

LUCI版本：19.07（当日最新）

### 特性及功能：
1.Ofast编译

2.内置三款主题

3.插件包含：OpenClash，AdguardHome，微信推送，网易云解锁，SQM，网络唤醒，DDNS，UPNP，FullCone(防火墙中开启)，流量分载(防火墙中开启)，SFE流量分载(也就是SFE加速，防火墙中开启，且默认开启)，BBR（默认开启），irq优化，OLED屏幕支持，Zerotier，FRPC，FRPS，无线打印，流量监控

4.核心频率1.608GHz

### 固件预览：
<img src="https://cdn.jsdelivr.net/gh/project-openwrt/R2S-OpenWrt@master/PIC/app.png" width="1024" />

### 防呆指导：
<img src="https://cdn.jsdelivr.net/gh/project-openwrt/R2S-OpenWrt@master/PIC/offload.png" width="1024" />
<img src="https://cdn.jsdelivr.net/gh/project-openwrt/R2S-OpenWrt@master/PIC/fullcone1.png" width="1024" />
<img src="https://cdn.jsdelivr.net/gh/project-openwrt/R2S-OpenWrt@master/PIC/fullcone2.png" width="1024" />
<img src="https://cdn.jsdelivr.net/gh/project-openwrt/R2S-OpenWrt@master/PIC/fullcone3.png" width="1024" />

### OLED效果预览：
<img src="https://cdn.jsdelivr.net/gh/project-openwrt/R2S-OpenWrt@master/PIC/oled.jpg" width="1024" />
