# Hackintosh EFI文件
## OpenCore版本

[OpenCore-0.7.0-RELEASE](https://github.com/acidanthera/OpenCorePkg/releases/tag/0.7.0)

## 适用范围

本EFI仅在本人ASUS TUF B460M +I5 10500 ES +RX5700 平台测试，不保证其它平台及同一平台不同环境下完全正常使用

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
10. USBMap.kext
11. [RealtekRTL8111.kext](https://github.com/RehabMan/OS-X-Realtek-Network)
12. [BrcmFirmwareData.kext](https://github.com/acidanthera/BrcmPatchRAM)
13. [BrcmPatchRAM3.kext](https://github.com/acidanthera/BrcmPatchRAM)
14. [CPUFriend.kext](https://github.com/acidanthera/CPUFriend)
15. [HibernationFixup.kext](https://github.com/acidanthera/HibernationFixup)
16. [NightShiftUnlocker.kext](https://github.com/0xFireWolf/NightShiftUnlocker)
17. [NVMeFix.kext](https://github.com/acidanthera/NVMeFix)
18. [BrcmPatchRAM](https://github.com/acidanthera/BrcmPatchRAM)

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
15. 兼容博通BCM943224PCIEBT4(其余型号未测试)
16. FCPX核显加速（最新版BIOS开启共享显存设置为64M或以上）
17. USB3.0正常识别（若USB定制无效参见：[解除USB限制原来如此简单](https://www.isolves.com/it/rj/jy/2020-06-24/21445.html)，或启用驱动列表中的USBinjectAll和XHCI-unsupported以及Kernel中Quirks下的XhciPortLimit选项，两种方法二选一）
18. 正常引导macOS Big Sur
19. 删除部分小众驱动，需要的请在驱动列表中自提,同时注意其中含有部分过时驱动，请自行斟酌

## 存在问题

1. 关于本机中CPU型号不正常显示（不影响正常使用，这里显示型号为：3 GHz 六核Intel Core i9）
2. CPU不正常变频（不影响正常使用）
3. PS2键盘映射
4. 无图形引导界面（单纯懒得搞，想搞的可以自行百度很简单）
5. 不兼容macOS 12 Monterey

