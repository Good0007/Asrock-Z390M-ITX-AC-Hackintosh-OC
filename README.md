## Asrock-Z390M-ITX/AC-Hackintosh-OC 华擎Z390MITX 黑苹果OC 配置

[我的博客同步更新](https://www.chenweikang.top/?p=986 "左手代码右手诗")

### 更新记录
- 20200604-release-0.6.0

更新opencore 0.6.0 release，macOS 11.0 暂未测试；

更新相关驱动；

- 20200604-release-0.5.9

更新到opencore 0.5.9 release，自测可正常升级到 Catalina 10.15.5；

机型采用 iMac19,1 注入核显id 开启硬件加速，网卡dw1820a调试完美（dw1820a不同子型号可能会要用不同注入参数，为了防止折腾建议上拆机卡），默认配置加上了1820a驱动，如果没用到改网卡请自行去除驱动！

### 主机配置
- 机箱：某宝（魔神科技) ghost s1
- 电源：EVGA SFX 650w 金牌
- 主板：华擎 Asrock Z390M-ITX/ac
- CPU：i5 9400
- 显卡：技嘉Radeon RX 5500 XT GAMING OC 8GB
- 网卡：DW1820A (0vw3t3 – 0x0023)
- 内存：海盗船 DDR4 3200 16GBx2
- 硬盘：西数黑盘 sn750
- CPU风扇：猫扇


### BOIS设置
```
Primary Graphics Adapter -> PCI Express
CFG Lock -> Disabled
IGPU Multi-Monitor -> Enabled
XHCI Hand-off -> Enabled
Secure Boot -> Disabled
CSM -> Disabled
Above 4G Decoding -> Disable (这个不使用双显卡的情况下必须关闭, 不然和 CSM 设置冲突, 造成 Windows 无法启动)
```

### 安装和问题参考

- 配置里提供【config单核显】、【config核显+5500xt优化专用】、【config核显+通用显卡】，请根据个人情况更名后食用，否则可能无法正常启动；

- cpu有核显的务必在BOIS里设置多监视器(IGPU Multi-Monitor)为启用状态；

- 默认配置加入了1820A驱动，cs2网卡的用户请自行删除1820A驱动！

- 设置开机默认启动Mac： 偏好设置->启动磁盘 设置默认启动盘。
 
- 镜像下载：[黑果小兵博客镜像地址](https://mirrors.dtops.cc/iso/MacOS/daliansky_macos/ "黑果小兵镜像")

- 常见问题：[安装常见问题](https://blog.daliansky.net/Common-problems-and-solutions-in-macOS-Catalina-10.15-installation.html "安装常见问题")

- Etcher烧录工具：[Etcher烧录工具](https://www.balena.io/etcher/ "Etcher烧录工具")

- OCC：[OC配置可视化编辑工具](https://mackie100projects.altervista.org/download-opencore-configurator/ "OCC")

- 参考了：https://github.com/huijiewei/ASRock-Z390m-ITX-ac-Opencore

- OpenCore相关知识：[Xjn的博客](https://blog.xjn819.com/?p=543 "Xjn的博客")

### 已知bug

暂无

### 关联B365ITX配置
[华擎B365ITX黑苹果](https://www.chenweikang.top/?p=846 "华擎B365ITX黑苹果")

