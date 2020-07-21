# Hackintosh EFI文件
## OpenCore版本
[2020-07-20 OpenCore-0.6.0-DEBUG](https://github.com/williambj1/OpenCore-Factory/releases/tag/2020-07-20)
## 适用范围

本EFI仅在ASUS TUF B460M +I5 10500 ES +RX5700 平台测试，不保证其它平台完全正常使用

## 参考内容

[daliansky/OC-little](https://github.com/daliansky/OC-little)

[Xjn's Blog](https://blog.xjn819.com/?author=1)

## 驱动列表
1. [Lilu.kext](https://github.com/acidanthera/Lilu)
2. [WhateverGreen.kext](https://github.com/acidanthera/WhateverGreen)
3. [VirtualSMC.kext](https://github.com/acidanthera/VirtualSMC)
4. [SMCProcessor.kext](https://github.com/acidanthera/VirtualSMC)
5. [SMCSuperIO.kext](https://github.com/acidanthera/VirtualSMC)
6. [IntelMausi.kext](https://github.com/acidanthera/IntelMausi)
7. [AppleALC.kext](https://github.com/acidanthera/AppleALC)
8. [FakePCIID.kext](https://github.com/RehabMan/OS-X-Fake-PCI-ID)
9. [FakePCIID_Intel_HDMI_Audio.kext](https://github.com/RehabMan/OS-X-Fake-PCI-ID)
10. [NVMeFix.kext](https://github.com/acidanthera/NVMeFix)
11. RadeonBoost.kext
12. USBPorts.kext
13. [USBPower.kext](http://blog.xjn819.com/wp-content/uploads/2019/10/USBPower.kext_.zip)
14. [RealtekRTL8111.kext](https://github.com/RehabMan/OS-X-Realtek-Network)
15. [BrcmFirmwareData.kext](https://github.com/acidanthera/BrcmPatchRAM)
16. [BrcmPatchRAM3.kext](https://github.com/acidanthera/BrcmPatchRAM)

## 已修正

1. 华硕主板开机卡F1
2. 修复部件数据为 `6D04`所造成的S4睡眠秒醒
3. EC控制器仿冒
4. GPI0
5. 注入 `x86` 实现 `CPU` 电源管理
6. 注入 `SBUS` 设备
7. `PNP0200` `MCHC`  `PNP0C01` `PMCR`  `APP9876`部件缺失修补
8. 加载原生电源管理
9. 节能五项
10. Apple设备快充
11. 声卡驱动正常
12. 支持Realtek RTL8111/8168 B/C/D/E/F/G/H等（该驱动在安装前首先需要删除/S/L/E中的Realtek驱动，然后复制重建缓存。不需要可以删除或直接无视。）
13. BrcmPatchRAM对博通网卡支持
14. 请自行模拟NVRAM，参见：[Xjn's Blog](https://blog.xjn819.com/)中使用OpenCore引导黑苹果 3.1 模拟NVRAM

## 存在问题

1. 关于本机中CPU型号不正常显示
2. CPU不正常变频（不影响正常使用）
3. FCPX无核显加速
4. PS2键盘映射
5. USB3.0不识别
6. 无法引导macOS 11
7. 无图形引导界面
