[B站上的效果展示视频](https://www.bilibili.com/video/av56761847)
---
* 红灯闪烁是一个独立线程
* 绿灯闪烁是一个独立线程
* LCD 显示是 CubeMX 下调好的驱动（到 RTT 上仅改了一点点）

LCD 接线
---
> LCD 用的是 Arduino 的 `LCD Keypad`<br>
> `5v 供电`

LCD    | STM32
:----- | -----:
RW     | PB4
E      | PB3
RS     | PD3
D4     | PD4
D5     | PD5
D6     | PD6
D7     | PD7

三平台通用
---
> 详见 github 上 [project-generator](https://github.com/project-generator/project_generator.git) 项目。<br>
> 一个项目起初就做好兼容，`后续就没有所谓“GCC移植到MDK5”这样的问题。`

* 解决 CubeMX 生成工程，加入用户配置后，若误删工程则无法找回的问题。
* MDK5、IAR、GCC 工程（或 Makefile）按配置好的`*.yaml`文件自动生成。`不用维护工程，只维护代码就可以。`

工作流
---
> 工作流展示如何在 CubeMX 生成的工程中按需加入 RT-Thread。<br>
> `有关“工作流”的部分，我会在公众号上逐步推文。`

欢迎扫码关注我的公众号`MultiMCU EDU`。<br>
![](https://github.com/SuWeipeng/img/raw/master/gongzonghao.jpg)<br>
### `提示：在公众号“关于我”页面可加作者微信好友。`

