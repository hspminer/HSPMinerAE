![](/logo.png)

# HSPMiner

Nvidia GPU Miner for `Aeternity (AE)`mining.

## Download

[Download here](https://github.com/hspminer/HSPMinerAE/releases)

## Community support

QQ： 870349675

## Performance (stock frequency)

| Algorithm        |  Coin   | P106,1060  |  P104-8G   |  1070ti  |  1080ti  |   2080   |
| :--------------- | :-----: | :-------: | :--------: | :------: | :------: | :------: |
| cuckoo_ae        |   AE    |   120n/min    |    ...     |   ...   |   260n/min    |   ...   |


## Features

* Support Win7, Win10, Linux mining.
* Supporting the standard stratum agreement of the mining pool.
* Low cpu and pcie occupied.
* Includes 3% development fee.



## Requirements

- win7,win10,Linux system
  - Nvidia,10 series graphics card, 4G or above video memory (1050ti please use linux version)
  - Nvidia driver version>398 (some users use 41X driver will be very slow, it is recommended to use 39X driver)
  - windows requires more virtual memory space than all memory sizes (for example, you have 1060 6G cards, at least 12G of virtual memory)



#How to use
- Windows system
  - Open the run.cmd file with txt file
  - Replacement-wal after the wallet address
  - (Optional) Replace the machine name after the -worker (usually used to distinguish the machine)
  - (Optional) Replace the pool address and port behind the -pool
  - (Optional) Replace the password for the connection pool behind -psw
  - Save, click to start run.cmd
  - (Optional) Click WebMonitor.cmd to open the browser (or open the browser directly) to view the mining status (in the presence of the -api parameter)

- Linux system
  - Open the run.sh file with a text editor
  - Replacement-wal after the wallet address
  - (Optional) Replace the name after the -worker (usually used to distinguish the machine)
  - (Optional) Replace the pool address and port behind the -pool
  - (Optional) Replace the password for the connection pool behind -psw
  - Save, console run./run.sh
  - (Optional) Click WebMonitor.cmd to open the browser (or open the browser directly) to view the mining status (in the presence of the -api parameter)


## Sample Usages

#### AE

- **f2pool:** HSPMinerAE.exe -pool ae.f2pool.com:7898 -wal {ae wallet address} -worker {worker name} -logfile -m 10 -api 0.0.0.0:16666
- **uupool:** HSPMinerAE.exe -pool ae.uupool.cn:6210 -wal {ae wallet address} -worker {worker name} -logfile -m 10 -api 0.0.0.0:16666
- **beepool:** HSPMinerAE.exe -pool ae-pool.beepool.org:9505 -wal {ae wallet address} -worker {worker name} -logfile -m 10 -api 0.0.0.0:16666

## CMD options：
-	-wal		AE mining Wallet Address
-	-worker		AE mining machine name
-	-pool		AE pool address, add tls://pool_url:port to enable TLS connection
-	-psw		AE Mining Pool Password
-	-device		AE mining enabled devices, defaults to all devices, with -bdevice 0, 2, 4 to limit running on GPU0, 2, 4 only

##Run information:
-	-api		Enable the network monitoring address, such as: 192.168.1.2:16666, use the browser to access http://192.168.1.2:16666, monitor the mining machine operation
-	-logfile	Enable the log file, the default is to generate the file name according to the time, followed by the file name to specify the file, such as -logfile hspminer.log
-	-hide		Hide the interface immediately after starting the program, note that it will run in the background. If you open the api interface, you can click WebMonitor.cmd to start the browser monitoring (not available under Linux)

### Web Monitor

Open http://api_host:port/ in your browser to use web monitor.


## Change Log

#### HSPMinerBTM 2.2.4 2019/1/2

- Fix:Fix some bugs

