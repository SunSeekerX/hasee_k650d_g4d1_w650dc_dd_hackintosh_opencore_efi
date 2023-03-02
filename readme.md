# OpenCore for hasee K650D-G4D1

![product-01](./assets/2015053002216853.png)

## 简介

已经完美了 🤣。

|       Key        |                                                    Value                                                     |
| :--------------: | :----------------------------------------------------------------------------------------------------------: |
| OpenCore version |                                                    0.8.9                                                     |
|  MacOS version   |                                            Ventura 13.2.1 (22D68)                                            |
|     机型官网     | http://archive.hasee.com/Chinese/product/index.aspx?cid=105001002003&yid=100000002923127&eid=100000013446143 |

开机界面示例：

![07114713](./assets/02093335.webp)

CFGLock 检查和部分 bios 设置：

| Describe        | Screenshot                                                   |
| --------------- | ------------------------------------------------------------ |
| CFGLock         | <img src="./assets/02093341.webp" alt="02093341" style="zoom:25%;" /> |
| VerifyMsrE2     | <img src="./assets/02093346.webp" alt="02093346" style="zoom:25%;" /> |
| Bios - Main     | <img src="./assets/WechatIMG26.webp" alt="WechatIMG26" style="zoom:25%;" /> |
| Bios - Advanced | <img src="./assets/WechatIMG27.webp" alt="WechatIMG27" style="zoom:25%;" /> |
| Bios - Security | <img src="./assets/WechatIMG28.webp" alt="WechatIMG28" style="zoom:25%;" /> |
| Bios - Boot     | <img src="./assets/WechatIMG29.webp" alt="WechatIMG29" style="zoom:25%;" /> |

## Bios 设置

- 硬盘模式改 AHCI
- Advanced -> Power and performance -> CPU Power management control -> CPU Lock configuration  -> Disable
- Advanced -> Advanced chipset control -> Fast boot -> Disabled 
- Advanced -> Advanced chipset control -> Sw Guide extensions -> Disabled 
- Advanced -> Advanced chipset control -> VT-D -> Disabled 
- Security -> Secure Boot -> Disabled 
- Boot -> Uefi Setting -> Uefi boot -> enable 
- Boot -> Uefi Setting -> Lunch csm -> Disable 

## 安装说明

- **我的 bios 是 D 大修改过的 bios，我自己修改解锁了 CFGLock 选项，更换了 CPU 为 i3-8100**

- **wifi 需要使用 HeliPort 进行链接，AirportItlwm 需要等待作者更新，目前在 13.x 系统开机需要等好久才能链接到 wifi。**
- **需要关闭 CFGLock，如果无法关闭需要勾选两个选项，自行 Google**
- 记得换三码，里面没有自带的
- 不要换机型，否则 usb 接口无法使用，需要替换 USBPorts.kext 内 plist 的机型值，你会写代码的话很简单打开改下两个地方就行
- 已经用来写了几天的代码，没啥问题。能开发，这个项目也是在 mac 下系统下传上来的

## 硬件

|         Key         |                                                     Value                                                      | Other                 |
| :-----------------: | :------------------------------------------------------------------------------------------------------------: | --------------------- |
|         CPU         |                                    Intel(R) Core(TM) i3-8100 CPU @ 3.60GHz                                     | 4 核 4 线程，3.60 GHz |
| 主板型号/准系统型号 |                                                   W650DC,DD                                                    |                       |
|        显卡         |                                             Intel UHD Graphics 630                                             |                       |
|       显卡 2        |                                           NVIDIA GeForce GTX 950M 4G                                           | 黑苹果已经屏蔽        |
|        内存         |                                         Samsung DDR4 2400 MHz 8 GB X 2                                         | 总共 16GB             |
|      无线网卡       |                          Intel(R) Dual Band Wireless-AC 3165 (10.0 [ TRIAL VERSION ])                          |                       |
|      有线网卡       |                           RTL8111/8168/8411 PCI Express Gigabit Ethernet Controller                            |                       |
|        声卡         |                Realtek ALC269 @ Intel Sunrise Point PCH - High Definition Audio Controller [D1]                |                       |
|       显示屏        |                                                       ~                                                        |                       |
|       触控板        |                                                       ~                                                        |                       |
|        硬盘         |                           WDS250G2X0C-00L350 (250 GB, PCI-E 3.0 x4)<br/>PCI-Express                            |                       |
|        接口         | USB3.0 X3<br/>USB2.0 X1<br/>HDMI X1<br/>RJ45 网口 X1<br/>VGA X1<br/>SD 卡槽 X1<br/>电源 X1<br/>耳机耳麦口各 X1 |                       |

## 正常工作

- CPU 正常睿频
- 英特尔网卡
- 声卡
- 触摸板（支持手势）
- 睡眠
- 核显正常驱动，支持缩放/调节亮度/夜览
- USB 接口完成定制

## 存在的问题

- 触摸板手势识别不是很灵敏

## 部分系统截图

![iShot_2023-02-07_19.00.14](./assets/iShot_2023-03-02_16.58.41.webp)

程序坞

![iShot_2023-02-07_20.13.57](./assets/iShot_2023-03-02_16.59.17.webp)

| Describe   | Screenshot                                                   |
| ---------- | ------------------------------------------------------------ |
| 静音       | <img src="./assets/iShot_2023-03-02_16.59.44.webp" style="zoom:25%;" /> |
| 亮度快捷键 | 不能用 🥵                                                     |
| Nvme       | <img src="./assets/iShot_2023-03-02_17.00.19.webp" style="zoom: 50%;" /> |
| USB        | <img src="./assets/iShot_2023-03-02_17.00.38.webp" style="zoom:50%;" /> |
| 以太网     | <img src="./assets/iShot_2023-03-02_17.00.50.webp" style="zoom:50%;" /> |
| 内存       | <img src="./assets/iShot_2023-03-02_17.01.55.webp" style="zoom:50%;" /> |
| 显卡       | <img src="./assets/iShot_2023-03-02_17.01.59.webp" style="zoom:50%;" /> |
| 摄像头     | <img src="./assets/iShot_2023-03-02_17.02.03.webp" style="zoom:50%;" /> |
| 电源       | <img src="./assets/iShot_2023-03-02_17.02.17.webp" style="zoom:50%;" /> |
| 蓝牙       | <img src="./assets/iShot_2023-03-02_17.02.28.webp" style="zoom:50%;" /> |
| 读卡器     | ~                                                            |
| 音频       | <img src="./assets/iShot_2023-03-02_17.02.47.webp" style="zoom:50%;" /> |
| WIFI       | <img src="./assets/iShot_2023-03-02_17.03.23.webp" style="zoom:50%;" /> |

## 部分 efi 截图

| Describe | screenshot                                                                 |
| :------: | -------------------------------------------------------------------------- |
|   ACPI   | ![iShot_2023-03-02_17.04.18.webp](./assets/iShot_2023-03-02_17.04.18.webp) |
|    Dp    | ![iShot_2023-03-02_17.04.36.webp](./assets/iShot_2023-03-02_17.04.36.webp) |
|  Kernel  | ![iShot_2023-03-02_17.04.52.webp](./assets/iShot_2023-03-02_17.04.52.webp) |

## 更新日志

### 2023-03-02

- 第一个可用的版本
