
 
[OpenWrt DIY — 固件云编译](https://jq.qq.com/?_wv=1027&k=9Sh2iNhT)
==============================================================================================================

请 `耐心认真阅读完毕` 本页面，本页面包含如何提升固件下载及使用体验的内容。

如果您未阅读完本页面，可能会遇到 `固件下载问题` ，若遇到问题，请 `返回此页面，认真完整阅读一遍`~




## 基本介绍 [![](https://img.shields.io/badge/-项目基本介绍-FFFFFF.svg)](#基本介绍-)

1. 默认引用[ Lean 的 OpenWrt 库](https://github.com/coolsnowwolf/lede)（部分设备整合[ Lienol 的 Packages 库](https://github.com/Lienol/openwrt-packages)），因为他的 [README](https://github.com/coolsnowwolf/lede/blob/master/README.md) 影响了我开始学习编译；Github Actions 自动云编译代码采用 [P3TERX 的 Actions-OpenWrt 库 ](https://github.com/P3TERX/Actions-OpenWrt)。

2. [插件及功能预览 请点击查看](https://github.com/IvanSolis1989/OpenWrt-DIY/wiki/OpenWrt-DIY%E6%8F%92%E4%BB%B6%E9%A2%84%E8%A7%88)

3. `每周五查询大雕源码是否有更新`，如有更新自动拉取最新源码和第三方软件包项目自动编译（根据设备不同编译时间在1~5个小时），`固件包含必要驱动及常用插件`（各设备的 config 借鉴大雕设置及根据网友需求调整），未逐一经过实机测试，故 `不保证 100% 可靠性`；

4. 如有什么问题、需要增加编译设备或者编译文件配置需要调整的，可以直接在 [Issues](https://github.com/IvanSolis1989/OpenWrt-DIY/issues) 内留言。 我会不定时的根据大家的要求修改`编译配置，插件选项，增加编译设备`等；

5. 为了让更多朋友的设备能用上稳定且功能强大的 OpenWrt 固件，并保持持续更新。也希望动手能力强的朋友去学习编译[（后文有教程）](#小贴士-)，然后根据你自己的需要配置 menuconfig，把配置好的 config 文件提交到本项目，可以根据使用者的需求扩充更多设备。

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-FFFFFF.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>



## 注意事项 [![](https://img.shields.io/badge/-下载注意事项-FFFFFF.svg)](#注意事项-)

1. 在固件编译完成后，会上传一份副本到 WeTransfer 和 奶牛快传，对于国内网络用户，为提高下载体验，可下载存放于这两个网站中的固件副本，副本下载地址位于固件下载页面中固件文件列表下的 Annotations 提示框内，`一段时间后（1~3天）网盘内的文件会失效`，所以推荐周五~周日下载最新版；
<details>
 <summary>&nbsp;&nbsp;&nbsp;找不到？请点击这里！</summary>
 
<br/>
<div align=center><img src="https://img.vim-cn.com/ef/2481045f0a6fac8ee6c0c437b5c225ee880295.png" alt="图裂了😂需要机场才能正常显示"/></div>
<div align=center><img src="https://img.vim-cn.com/f8/d5f01cc3e33460963635eb7b7cf5a472859f88.png" alt="图裂了😂需要机场才能正常显示"/></div>
</details>

2. 在极少数情况下，因网络原因这两份副本可能会上传失败，如果遇到这种情况，就只能下载存放在 Github Action 里的固件了，由于 Github Action 限制，`需要登录 Github 账号才可下载存放于 Github Action 中的固件 (未登录时固件链接不可被点击)`，但 WeTransfer 和 奶牛快传 的固件下载链接在未登录状态下可正常查看，不受影响；

3. 如果需要下载存放于 Github Action 上的固件，由于众所周知的原因，`请尽量使用科学上网方式下载固件`，固件下载完成后，请下载 sha256sums 文件或使用压缩软件的 "测试压缩文件" 功能来验证固件的完整性。

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-FFFFFF.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>

## 小贴士 [![](https://img.shields.io/badge/-日常使用技巧及教程-FFFFFF.svg)](#小贴士-)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 本栏目包含了很多 OpenWrt 日常使用问题解决方案、“不可描述”的教程、广告屏蔽教程，NAS（或路由器共享盘）的多媒体文件整理播放教程、OpenWrt 本地自编译教程。

<details>
 <summary>&nbsp;&nbsp;&nbsp; 基础常用</summary>

<br/>

[OpenWrt 基础配置](https://github.com/IvanSolis1989/OpenWrt-DIY/wiki/OpenWrt-%E5%9F%BA%E7%A1%80%E9%85%8D%E7%BD%AE)

[OpenWrt 软路由 IPv6 上网设置](https://github.com/IvanSolis1989/OpenWrt-DIY/wiki/OpenWrt-%E8%BD%AF%E8%B7%AF%E7%94%B1-IPv6-%E4%B8%8A%E7%BD%91%E8%AE%BE%E7%BD%AE)

[OpenWrt 网络共享文件和 Transmission 使用技巧，再也没有恼人的权限问题](https://youtu.be/wmR7o9p9vSY)

[SD 卡设备固件刷写程序 BalenaEtcher](https://www.balena.io/etcher/)

</details>

<details>
 <summary>&nbsp;&nbsp;&nbsp; USB 网卡</summary>

<br/>

**USB 有线网卡**

推荐使用基于 AX88179（[绿联20256](https://union-click.jd.com/jdc?e=&p=AyIGZRprFQETA10cXSVGTV8LRGtMR1dGFxBFC1pXUwkEAEAdQFkJBVsWAxYPUh1ETEdOWmVdIHFbakcpHD4LGBJsV3suc1ducxNNVxkyEzdWGlsVBhcEVRNYJTISAGVNNRUDEwZUGlgTAhQ3VCtbEgIRAVATUxYCEQdUK1wVCyJcAHVfRVBCUAEYXBQFQQICK2slASI3ZRtrFjJQaVRIWRIEEAZRGQsRUhdVABkLEVIQV1xIDhYDFQdQElkTMhAGVB9S)）或 RTL8153（[山泽UW013](https://union-click.jd.com/jdc?e=&p=AyIGZRtYFAUWA1MdXBYyFQVTH14UByJDCkMFSjJLQhBaGR4cDF8QTwcKWUcYB0UHCwUQAVEeWhAdS0IJRmt9dE9wLGwwV2JUUyliWBxEDEdQGilTDh43VCtYFAISA1AYWx0BIjdVHGtXbFBXCVACQVlKTwErWiUCFQdWHV4dChYBUhtZJQUSDmVADnsGQlUFTA8WBRMABh4MJTIiBGUraxUyETcXdVkcBhIHUxxSFAcXB1AeCBALGwJdEgxHCxpQVhpTRQERN1caWhEL)） 芯片的 USB 有线网卡设备。

**USB 无线网卡**

推荐使用基于雷凌 RT3070(150Mbps)/RT5370(150Mbps)/RT5572(300Mbps+600Mbps) 芯片;  

或 MT7612U(300Mbps+867Mbps) 芯片的 USB 无线网卡设备 (例如华硕 AC55、网件 A6210 等)。

**备注**：个人不建议在软路由设备上用 USB 外接无线网卡，信号强度、稳定性都比较弱。

</details>

<details>
 <summary>&nbsp;&nbsp;&nbsp; 不可描述</summary>

<br/>

[最好的 OpenWrt 路由器 shadowsocks 自动翻墙、科学上网教程](https://github.com/softwaredownload/openwrt-fanqiang)

[自由上网方法大全](https://github.com/Alvin9999/new-pac/wiki)

[Clash for Windows](https://github.com/Fndroid/clash_for_windows_pkg)

[WinXray](https://github.com/TheMRLL/winxray)

[翻墙软件 VPN 推荐指南（含 2020 优惠）](https://github.com/vpncn/vpncn.github.io)

[免费机场节点获取 1](https://github.com/hugetiny/awesome-vpn/blob/master/READMECN.md)

[免费机场节点获取 2](https://bu.link2.workers.dev/https/github.com/freefq/free)

</details>

<details>
 <summary>&nbsp;&nbsp;&nbsp; 广告屏蔽</summary>

<br/>

[anti-AD 中文区命中率最高的广告过滤列表](https://github.com/privacy-protection-tools/anti-AD)

[最完善的 iOS 翻墙规则](https://github.com/h2y/Shadowrocket-ADBlock-Rules)

[国内加速过滤广告规则订阅](https://github.com/Silentely/AdBlock-Acceleration)

[AdGuard Home 更新好内核后，启动提示未运行、未重定向解决方法](https://www.vediotalk.com/archives/29410)

[AdGuard Home 规则大全](https://github.com/IvanSolis1989/OpenWrt-DIY/wiki/AdGuard-Home%E8%A7%84%E5%88%99%E5%A4%A7%E5%85%A8)

</details>

<details>
 <summary>&nbsp;&nbsp;&nbsp; NAS 影院</summary>

<br/>

[最NB的家庭影院播放器KODI](http://www.kodiplayer.cn/)

[全球5000多个IPTV频道](https://github.com/iptv-org/iptv)

</details>

<details>
 <summary>&nbsp;&nbsp;&nbsp; 本地编译</summary>

<br/>

[基本编译教程](https://blog.csdn.net/Dreame_Architect/article/details/101527640)

[WIN10 内置 Ubuntu 子系统编译教程](http://www.fuweijun.com/index.php/2019/07/03/win10%E5%AD%90linux%E7%B3%BB%E7%BB%9F%E7%BC%96%E8%AF%91openwrt/)

[Win10 子系统 Ubuntu18.04 下编译 OpenWrt 问题及解决方法](https://blog.csdn.net/khaunag/article/details/104854536)

[Ubuntu 默认源更新慢可更换清华大学镜像源](https://mirror.tuna.tsinghua.edu.cn/help/ubuntu/)

[Lean's OpenWrt 插件大全](https://github.com/IvanSolis1989/OpenWrt-DIY/wiki/Lean‘s-OpenWrt-——LuCI-Applications-插件说明)

</details>

<a href="#readme">
    <img src="https://img.shields.io/badge/-返回顶部-FFFFFF.svg" alt="图裂了😂" title="返回顶部" align="right"/>
</a>




## 鸣谢 [![](https://img.shields.io/badge/-跪谢各大佬-FFFFFF.svg)](#鸣谢-)
 
[OpenWrt 官方库](https://github.com/openwrt/openwrt)

[P3TERX 的 Action 库](https://github.com/P3TERX/Actions-OpenWrt)

[Lean 的 OpenWrt 库](https://github.com/coolsnowwolf/lede)

[Lienol 的 Packages 库](https://github.com/Lienol/openwrt-packages)

[SuLingGG 的 OpenWrt-Rpi 库](https://github.com/SuLingGG/OpenWrt-Rpi)



