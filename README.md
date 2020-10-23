# opencore-M420

我的 openCore 配置文件

型号： 联想-M420

* CPU: Intel第九代酷睿 HexaCore Intel Core i5-9500, 4300 MHz (43 x 100)
* 主板名称 Lenovo 313A
* 芯片组	Intel Cannon Point B360, Intel Coffee Lake-S
* 显示适配器   Intel(R) UHD Graphics 630  (1 GB),1个VGA、1个HDMI，两个接口分别接了两个显示器。
* 音频适配器 Realtek ALC662 @ Intel Cannon Point PCH - cAVS (Audio, Voice, Speech) [B0]
* 蓝牙无线：BCM94360CD Broadcom BCM4360 802.11ac Wireless Network Adapter
* 硬盘	500GB SATA接口 SSD  256GB M.2接口 NVMe协议 SSD
* DDR4 SDRAM  外部频率 1333 MHz (DDR)
* Realtek RTL8168/8111 PCI-E Gigabit Ethernet Adapter

* openCore 版本： 0.6.2


### 注意：

1. 蓝牙驱动需要 USBInjectAll.kext，但 usb 定制后就可以不用了。

### 解锁 CFG Lock 

参考 https://github.com/cheneyveron/hackintosh-clover-z390-aorus-pro-wifi-9700k-rx580/blob/master/README.md
```
CFG Lock, VarStoreInfo (VarOffset/VarName): 0x656, VarStore: 0x1, QuestionId: 0xAED, Size: 1, Min: 0x0, Max 0x1, Step: 0x0 {05 91 C1 03 C2 03 ED 0A 01 00 56 06 10 10 00 01 00}		
```

CFG Lock 地址为：0x656

### 加入 EFI.CFG 目录用于解锁 CFG Lock，使用这个 EFI 启动后，输入 `setup_var 0x656 0x00` 即可解锁。

