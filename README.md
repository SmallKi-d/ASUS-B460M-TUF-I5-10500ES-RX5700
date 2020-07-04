# Hackintosh EFI文件
## 适用范围

本EFI仅在ASUS TUF B460M +I5 10500 ES +RX5700 平台测试，不保证其它平台完全正常使用

## 参考内容

[daliansky/OC-little](https://github.com/daliansky/OC-little)
[Xjn's Blog](https://blog.xjn819.com/?author=1)

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

## 存在问题

1. 关于本机中CPU型号不正常显示
2. CPU不正常变频（不影响正常使用）
3. FCPX无核显加速
4. 无蓝牙驱动
5. 无Wi-Fi驱动
6. 无声卡定制（HDMI显示器只会出现系统提示音，耳机只会出现媒体音）
7. PS2键盘映射
8. 部分非免驱有线网卡未驱动（本人Intel I219V12 免驱）
9. 开机自检错误
10. USB3.0不识别
