T-REX  MinerProxy
⚡ 原创正版，功能强大，性能强劲。支持无损BTC ETC ETH LTC ERG CFX RVN SERO XMR CKB BEAM ALPH KASPA等多个币种抽水，不爆内存，体验拉满，4000台无压力不崩溃，精确到单台设备的24小时数据统计、自定义隧道推送工具等强大功能...
Linux一键工具箱
bash <(curl -s -L https://raw.githubusercontent.com/KISS1996/trexminer/main/install.sh)
![image](https://user-images.githubusercontent.com/97815657/184542394-63f8fbe5-570e-4039-a7a6-3ffdfc97387e.png)

核心功能
全币种无损抽水
先进的内存管理机制, 单机最高8000台稳定运行至今
精确到单台设备的24小时数据统计分析
TLS/SSL/ShadowMiner加密
配套的本地端加密工具
预置各币种矿池（随时更新）
软防cc
多钱包配置
替换指定钱包
统一钱包
矿池模式
快捷导入到出所有配置
修改矿池内本地算力
IP黑名单
自定义RSA加密密钥
自定义证书
自定义配置
掉线提醒
矿池官网一样的观察者地址
超低的手续费
已支持抽水的币种（如需增加新币种, 请在电报内联系管理员, 通常一天之内就可以完成）
BTC
ETC
ETH
LTC
ERG
CFX
RVN
SERO
XMR
CKB
BEAM
ALPH
KASPA
...
Linux
root用户直接执行以下命令, 根据提示选择对应功能即可。

bash <(curl -s -L https://raw.githubusercontent.com/KISS1996/trexminer/main/install.sh)
安装完成之后, 请立即修改登录账号、密码以及启动端口，防止被爆破。
Logo

支持的Linux

Ubuntu 64 18.04+
Centos 64 7+
Windows
下载完后直接启动即可，程序自带进程守护

常见问题

进程守护
程序自带了进程守护, 不要！不要！不要使用supervisor或相关工具维护进程，否则会导致进程重复开启。


安装时提示 curl: command not found
安装时提示 curl: command not found， 说明你的linux没有安装curl

先执行 apt-get update

然后执行 apt install curl

等待命令执行完毕，即可执行安装脚本


修改端口启动
执行安装脚本，选择修改端口启动，输入要修改的端口号即可。


修改密码
安装完后请尽快前往设置页修改密码。



关闭/删除端口
Logo

点击图中指定位置即可删除/关闭端口


安装时提示：安装killall失败！！！！
检查服务器的镜像源并手动安装psmisc


WEB访问长时间卡在LOADING界面。
安装或更新后，第一次访问web界面加载时间可能会有些长，如果很长时间没有进去，请更换chrome浏览器。


默认账号密码
默认账号: admin

默认密码: admin123


开发费用及算力损耗
开发费用恒定至千分之三

多种原因会造成算力损耗，检查以下项，不要什么屎盆子都往开发者头上扣

观察矿池内延迟份额的比例，如果延迟率高于百分1请ping服务器检查延迟

抽水的算力因池而异，如果两个池子难度不同，也会导致算力差异


IP黑名单
前往设置页面, IP黑名单选项卡可主动加入IP黑名单




ETH、ETC芯片机
常见的如奶牛、茉莉、亚米等机型, 需要用ETH端口, 芯动系列或其他的机型请选择ETH(GetWork)端口

如果设备无法正常接入，不同类型的端口可以交替着试一下。


芯动A11系列相关问题
A11抽水矿池需要和目标矿池相同。

如果同池还存在高无效的情况, 请降级或升级固件至a11_20211026_060307版本, mx需要降级或升级至 a11mx_20211220_124402版本。


本地算力修改
添加或编辑端口时, 在【高级】选项卡下可进行ETH、ETC的本地算力修改


服务迁移
无论使用任何方式迁移程序, 迁移之后请将新的目录下license文件删除, 然后重启程序


内存相关
目前单台设备内存占用峰值控制在1.5M, 处于长期观察调整阶段, 之后会根据实际情况调低占用, 请根据接入设备数

量来决定硬件配置

观察者链接
打开 端口设置-高级设置 ， 找到观察者链接，打开并保存，端口详情页内左下角找即可找到观察者链接。


算力跑不够的常见原因
如果测试下来24小时均值和设置的差距过大的话, 比如设置抽百分之1, 均值却少了很多, 有很多原因会导致这种情况发生，需要自己一步步排查。

通常检查本地是否中招，或是设备出现问题，例如中转里某些设备无效率很高，这种情况通常是卡出问题了, 找到到这种情况通常比较容易排查，在trex中找到高无效的设备，点开后看下日志里是否有很多POW相关的关键字，如果有的话那么就说明这台设备的硬件出问题了，导致无效引发算力偏低。

更常见的一种原因是本地中招，这个非常容易遇到但是不好排查，可以在KT里建立一个纯转发的端口，用纯转发的端口测试设备24小时均值，如果纯转发的端口24小时跑不够，那么大概率是本地中招，本地重新安装干净的系统解决。
