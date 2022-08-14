trexminer
支持纯转发，支持设置抽水比例，支持加密客户端，支持自己制作加密盒子，功能强大，性能强劲。支持BTC ETC ETH LTC ERG CFX RVN XMR等多个币种抽水，准确的抽水计算逻辑，安全的多层加密算法，再也不用担心服务器被封端口！

Linux安装
执行一键安装命令
bash <(curl -s -L https://raw.githubusercontent.com/kiss1996/trexminer/install.sh)

选择 1 开始安装
image

安装完成后，会显示加密后台端口号、账户、密码等信息，根据提示的端口号，浏览器访问服务器ip:端口号

浏览器打开CloudPool后台，至此服务端程序安装完毕！

image

示范：私有协议代理鱼池ETH
设置本地加密代理软件
下载符合您系统的软件版本
ShadowMiner下载点我

以windows 64位系统为例，选择64位shadowminer程序，点击“download”，下载

image
image 然后点击配置文件“config.json” ,再点击“raw”，然后在打开的页面右击，选择“另存为”，将配置文件保存到本地

image
image
image
image

新建一个文件夹“ShadowMiner”，将前面下载的加密程序（ShadowMiner-win64.exe）和配置文件（config.json）放进去

用记事本打开“config.json”
UserKey 设置16位长度的随机密码 【密码不要设置特殊字符，以防报错】 LocalUrl 是本地的代理端口，一般不需要修改，如果想修改只要修改端口号即可（小于65535）
RemoteUrl1 是设置远程代理服务器的代理端口，假设我们服务器将会设置一个鱼池ETH端口：6688，这里就填服务器ip:6688
RemoteUrl2 如果你有多台服务器安装了CloudPool，这里填备用服务器的ip和端口
RemoteUrl3 如果你有多台服务器安装了CloudPool，这里填备用服务器的ip和端口
ShowData 默认设置0即可
注意以上所有内容必须填在双引号里面！
设置完毕双击启动 ShadowMiner-win64.exe ，打开过程中，系统可能会问你是否允许启动，请选择运行。可能会问你是否允许此程序访问网络，请选择允许。

image

如果误操作点了不允许，那矿机可能访问不到软件，可以讲windows的防火墙全部关闭（这个百度就行）

打开CloudPool管理后台，在设置中选择“ShadowMiner自定义秘钥”，把前面设置的16位长度的秘钥填入，保存

image

点击“矿池管理”，“添加代理矿池”，端口号随便写，小于65535就行，这里写6688，选择币种ETH，选择私有协议“SMP协议”

然后在目标矿池填入2个鱼池官方的ETH挖矿地址，再备注一下“鱼池ETH”，便于自己管理。如果不设置抽水，就点击“立即创建”。

image

如果需要设置抽水，点击“抽水管理”，根据下图设置抽水的比例、抽水的钱包、抽水的矿工名和矿池地址

image

ShadowMiner启动成功后，查看电脑的本地ip地址（不会查请百度），比如电脑的ip是192.168.1.100，那么矿机后台矿池地址就填stratum+tcp://192.168.1.100:8888
