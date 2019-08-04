![](/logo.png)

# HSPMiner

用于显卡GPU的`Aeternity (AE)`挖矿软件。

## 下载地址

[从这里下载](https://github.com/hspminer/HSPMinerAE/releases)

## 社区支持

官方QQ群： 870349675

## 参考算力（默认频率）

| 算法             |  币种   | P106,1060  |  P104-8G   |  1070ti  |  1080ti  |   2080   |
| :--------------- | :-----: | :-------: | :--------: | :------: | :------: | :------: |
| cuckoo_ae        |   AE    |   120n/min    |    ...     |   ...   |   260n/min    |   ...   |


## 功能特点

- 支持Windows和Linux
- 支持标准协议的矿池
- 低CPU和pcie占用。
- 开发手续费:3%



## 配置需求

- win7,win10,Linux系统
  - Nvidia 10系列显卡，4G或以上显存（1050ti请使用linux版）
  - Nvidia驱动版本> 398（有些用户使用41X驱动会很慢，建议使用39X驱动）
  - Windows需要比所有内存大小更多的虚拟内存空间（例如，您有1060个6G卡，至少12G的虚拟内存）

- 显卡参数需求:

|       算法       |  币种   | Compute Capability | 显存 (Win7 & Linux) | 显存 (Win10) |
| :--------------: | :-----: | :----------------: | :-----------------: | :----------: |


#使用方法
- Windows系统
  - 使用记事本打开run.cmd文件
  - 替换-wal 后的钱包地址
  - (可选)替换-worker 后的旷工名称(一般用于区分机器)
  - (可选)替换-pool 后面的矿池地址和端口
  - (可选)替换-psw 后面的连接矿池的密码
  - 保存,点击启动run.cmd
  - (可选)点击WebMonitor.cmd启动浏览器(或直接启动浏览器),可查看挖矿状态(-api参数存在情况下)
- Linux系统
  - 使用文本编辑器打开run.sh文件
  - 替换-wal 后的钱包地址
  - (可选)替换-worker 后的旷工名称(一般用于区分机器)
  - (可选)替换-pool 后面的矿池地址和端口
  - (可选)替换-psw 后面的连接矿池的密码
  - 保存,控制台运行./run.sh
  - (可选)WebMonitor.sh启动浏览器(或直接启动浏览器),可查看挖矿状态(-api参数存在情况下)


## 使用样例

#### AE

- **beepool:** HSPMinerAE.exe -pool ae-pool.beepool.org:9505 -wal {替换钱包地址} -worker {替换旷工名称} -logfile -api 0.0.0.0:16666
- **f2pool:** HSPMinerAE.exe -pool ae.f2pool.com:7898 -wal {ae wallet address} -worker {worker name} -logfile -m 10 -api 0.0.0.0:16666
- **uupool:** HSPMinerAE.exe -pool ae.uupool.cn:6210 -wal {ae wallet address} -worker {worker name} -logfile -m 10 -api 0.0.0.0:16666

## 命令行参数
-	-wal		挖AE钱包地址
-	-worker	    挖AE旷工名称
-	-pool		挖AE矿池地址,可加tls://pool_url:port,启用TLS连接
-	-psw		挖AE矿池密码
-	-device	    挖AE启用的设备,默认为全部设备,可用-device 0,2,4来限制只在GPU0,2,4上运行

##运行相关:
-	-api		启用网络监控的地址,比如:192.168.1.2:16666,可用浏览器访问http://192.168.1.2:16666,监控矿机运行
-	-logfile	启用log文件,默认为根据时间生成文件名称,后面可跟文件名称来指定文件,比如-logfile hspminer.log
-	-hide		启动程序后立即隐藏界面,注意会在后台运行,如果开了api接口，可点击WebMonitor.cmd启动浏览器监控(Linux下不可用)

## API查询接口

### 网页监控

在浏览器中打开 http://api_host:port/ 启动网页监控.


## FAQ


#### 为什么我的矿池算力比本地算力低?

- `矿池的显示算力`


## 修改记录

#### HSPMinerAE 2.2.4 2019/4/17
- Add:提升算力0.5%-2%

#### HSPMinerAE 2.2.2 2019/4/14
- Fix:提升内核稳定性

#### HSPMinerAE 2.2.1 2019/4/12
- Add:提升性能1.2%
- Fix:尝试性修复内核重启问题(不一定解决)
