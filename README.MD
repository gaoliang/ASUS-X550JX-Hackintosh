# ASUS X550JX 黑苹果相关文件
## 简介
这是华硕X550JX（国内名称为飞行堡垒FX50JX)的黑苹果相关文件, 这套配置从16年的10.11一路升级到10.13。期间修改了许多驱动方法和配置，目前已经相对较完美。EFI中还包含了ubuntu16.04和windows的启动引导，如不需要可删除。
## 本机硬件
- CPU: intel i5-4200H
- 内存: 4GB板载 + 8GB金士顿DDR3
- 硬盘: OCZ TR150 256G SSD, SATA3接口
- 网卡/蓝牙：原始网卡无解，更换为可免驱的BCM43225HMB
- 显卡：HD4600,屏蔽N卡
## 哪些可以用？
- [x] CPU变频
- [x] 显卡硬件加速(QE/CI)
- [x] 亮度调节(小太阳)
- [x] 音频
- [x] HDMI输出
- [x] USB3.0 USB2.0
- [x] WIFI/蓝牙(需更换网卡)
- [x] 电量显示正常
- [x] 触控板（设置界面可能会异常）
- [x] 睡眠和唤醒
- [x] Fn快捷键

## 等待修复的问题
- [ ] 蓝牙连接蓝牙耳机时，有一定几率会出现wifi断开

## 相关驱动
黑苹果使用的开源驱动的地址和使用说明记录，方便以后的升级


| kext  | 功能 | 
| ---------- | -----------|
| [FakePCIID*](https://github.com/RehabMan/OS-X-Fake-PCI-ID)  |包括显卡，WIFI和USB等多种特性|
|[ACPIBatteryManager](https://github.com/RehabMan/OS-X-ACPI-Battery-Driver)|电量显示相关|
|[Lilu](https://github.com/vit9696/Lilu)|部分kext依赖的框架|
|[IntelGraphicsFixup](https://sourceforge.net/projects/intelgraphicsfixup/)|修复Intel集显的小问题|
|[AppleALC](https://github.com/vit9696/AppleALC)|声卡驱动|
|[AppleBacklightInjector.kext](https://www.tonymacx86.com/threads/guide-laptop-backlight-control-using-applebacklightinjector-kext.218222/)|亮度调节|
|[AzulPatcher4600.kext](https://github.com/coderobe/AzulPatcher4600)|修复开机和唤醒鼠标卡顿|
|||

还有部分没有写上的等待后续添加	
## 部分问题的解决记录
#### 10.12.4之后亮度无法调节的解决
使用AppleBacklightInjector.text代替之前的inetlBacklight.kext,[使用方法](https://www.tonymacx86.com/threads/guide-laptop-backlight-control-using-applebacklightinjector-kext.218222/)

## config.plist解析
todo