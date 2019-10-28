# MiPay 卡面工具

![下载](https://img.shields.io/badge/%E4%B8%8B%E8%BD%BD-%E9%85%B7%E5%AE%89-blue)

这是一个小工具，可以帮助你替换自己的 Mi Pay 卡面为自己想要的图片。

需要 Root 权限！<br />
需要 Root 权限！<br />
需要 Root 权限！

图片可以是 PNG GIF 等格式（没错，你甚至可以放动图）。

## 如何使用

### 替换卡面

1. **准备一些你喜欢的图片，作为素材。**

   如果你只用软件自带的卡面，则直接点击卡面，选择要替换的卡面即可。

   如果你只是萌新 / 只想简单地替换图片，请确保你准备的是横板，分辨率大于 960x606 的图片，将其保存到手机即可；

   如果你是大佬并打算自制卡面，请保证最终输出是 960x606 并带有 40px(39px?) 的圆角的成品卡面，并将做好的卡面传到手机（也可以不做圆角，让软件自动裁切）。

2. **打开本工具，点击「选择图片」并选择 图片 / 成品卡面**，或在图片查看器中把卡面「分享」到本工具，此时你有两种选择：

   - **勾选「裁剪后保存到列表」并选择「裁剪」**

     此时会调用可以裁剪图片的应用，如系统自带图库、照片编辑器、Google 相册、快图浏览等，可能个别图库应用裁剪会出现异常，你可以从应用商店安装上述应用中的其他应用进行裁剪。

     裁剪后的图片会被本软件自动剪圆角，并保存到 `/Pictures/MiPayCard/List` 下。此时，再点击列表中你刚才添加的卡面，选择你要替换的卡面。

   - 若是成品卡面，你也可以**选择「直接应用」**，选择你要替换的卡面。

3. （授予 Root 权限，）替换完毕，你可以打开你的 Mi Pay 刷卡界面查看效果了。

顺带一提，貌似交通卡的卡面大小是 960x606，而银行卡的卡面大小是 900x567。

### 提取卡面

点击右下角「+」号，点击提取卡面即可。

提取出的卡面会被保存在 `/Pictures/MiPayCard` 下，并附有一份 txt 用于说明卡面文件在缓存中的名称。

**如果需要提取原版卡面，请先「恢复默认卡面（同样在「+」号下）」再提取。**

### 在线卡面

在群主群友的不~~屑~~懈努力下，除了预置的本地卡面，软件添加了在线卡面的功能，并收集了一部分群友作品。

点击右上角的「相册」图标，或在「+」号中选择「在线卡面」即可进入在线卡面界面。

在此界面，你可以下拉刷新，以检查是否有新的在线卡面。此时右上角的「相册」图标可用于切换自制卡面和官方卡面（即各大银行卡面好康的卡面原图）；右上角的菜单中可查看相关说明 & 提交你自制的卡面。

点击一张在线卡面，你可以选择「设为卡面」、「添加到卡面列表」或者查看作者的信息。

如果卡面图是一片空白（而且你等了好几分钟还是一片空白），那么可能是卡面所在的图床炸了 / 卡面被虚无了，请联系开发者。

### 卡面设置方式

群友建议，因为软件并不知道 Mi Pay 界面缓存里的图对应的是什么卡叫什么名，所以不如干脆把卡图展现出来，取代旧版只显示一堆令人迷惑的文件名的显示方式。

解释如下：

- 默认：原来的显示方式，无图，只显示缓存文件对应的名称。如果卡面没有适配，需要自己先「提取卡面」以确认自己要替换的卡面叫啥名字，以免替换出错。
- 新-MiPay：新版显示方式，同时显示图片和卡面名称（如果有适配的话，还会显示卡片名称）。
- 新-小米钱包：用于替换小米钱包中显示的卡面，而不是 Mi Pay 界面的卡面，效果同上。

注意：小米钱包缓存中的各种杂七杂八的图片都会被显示出来，甚至还有银行卡的缩略图（如果你发现一张卡有两个对应的文件的时候，通常其中一张是缩略图），如果运气不好替换到的是缩略图，替换另一张即可。

目前推荐使用新版替换方式，界面不太完善和好看，勿喷。

### 卡面适配

虽然有了新版的卡面设置方式，卡面适配已经在某种意义上成为了过去式，但是我们仍然欢迎你提交卡面和具体的卡片名称，方便他人。步骤如下：

1. 安装一个邮箱应用（推荐 Gmail）

2. 注意留存自己的魔改卡面，「+」号，「恢复默认卡面」

   如果不进行这一步，开发者收到的就是你替换过的卡面而一头雾水。

3. 点击软件右上角菜单，「提交卡面适配」，「提交适配」

4. 编辑邮件，附上每一张未适配卡的名称，发送邮件

5. 坐等适配

### 缓存管理

由于在线卡面通常是原图，加载之后软件不会去自动删除，如果你想删除，可以在主界面右上角菜单「缓存信息」中查看当前在线卡面占用的空间大小，以及是否需要删除。

## Extra：Magisk 模块

为了保证卡面的显示效果，这里还准备了一点魔法：Magisk 模块。

特别感谢：酷安 @toolazy

| 模块 zip 名         | 模块作用                                            | 下载                                                         |
| ------------------- | --------------------------------------------------- | ------------------------------------------------------------ |
| hide_mipay_logo     | 屏蔽 Mi Pay 界面卡面右上角的 Mi Pay Logo            | [下载](https://github.com/gddhy/MiPayCard/raw/master/hide_mipay_logo.zip) |
| hide_miwallet_mipay | 屏蔽 小米钱包 - 银行卡 界面卡面右上角的 Mi Pay Logo | [下载](https://github.com/gddhy/MiPayCard/raw/master/hide_miwallet_mipay.zip) |

## 常见问题

1. - 为什么用不了？
   - 在？你 Root 了吗？

2. - 水印是啥？
   - 如果选择「添加水印」，软件会在图上添加卡片名称和 银联/交联 标志。

3. - 为啥我的卡面明明是适配过的，更新/刷机/…… 之后又没了？
   - 我也不知道啊…… 目前有的卡片（比如京东闪付）已经一大堆名称对应了但是还是没覆盖完，但是像上海交通卡之类的公交卡貌似适配还不错。

（更多问题待补充）

## 交♂流

| QQ 群（大概是大本营）                                        | Telegram 群                                              |
| ------------------------------------------------------------ | -------------------------------------------------------- |
| [【MI Pay卡片美化交流群】点击就进](https://jq.qq.com/?_wv=1027&k=51IWRSV) | [点击就进](https://t.me/joinchat/BwswvA36VrDoxdeLaXjrEg) |

BTW，这个 README 是 [星野みなと](https://github.com/Skimige) 写的。