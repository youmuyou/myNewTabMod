# myNewTabMod by sakuyaa

该扩展的WebExtension版本[myNewTabWE](https://github.com/sakuyaa/myNewTabWE)正在开发中。由于API的限制，部分功能无法实现，新的扩展需要重新进行配置。

首先感谢一下原作者`defpt`和`ywzhaiqi`:clap:，
这个扩展是根据[myNewTab](http://bbs.kafan.cn/thread-1759418-1-1.html)这个扩展修改而成的

## 主要的不同之处
1. 实现火狐41上设置为新标签页
* 将参数存放在火狐preferences里面
* 将导航配置、壁纸等可能有改动的文件设置在profile文件夹内，实现扩展签名
* 扩展重装后不会覆盖配置
* 替换日历算法为我自己编写的算法，从而准确显示父亲节:man:、母亲节:woman:这样的节日
* 可在扩展数据文件夹内自定义网页css
* 神秘的代码:underage:

## 可能造成不便的地方
1. 存放导航网址的数据文件data.txt中，为网址指定本地图标文件时需要以斜杠`/`开头
* 我写的农历算法由于是使用公式自动计算的缘故，可能会出现一些错误（已修复2010-2020年存在的误差）
* Bing壁纸的命名还是采取日期+壁纸的信息，不会自动删除，需要注意壁纸会一直累积下去
* 默认的导航网址中有返利链接
* 在火狐配置文件目录里的扩展数据文件夹中的自定义css文件并不会随着扩展目录的chrome\skin文件夹的默认css文件更新
* 扩展数据文件夹中自定义style.css文件优先级高于默认css文件，weather.css文件将直接覆盖默认css文件

## 扩展图文
* 扩展主界面，左上角的天气可以在附加组件管理器中该扩展选项界面设置其URL
	国历和农历日期会以不同颜色显示当天的节假日和节气信息
![](https://raw.githubusercontent.com/sakuyaa/myNewTabMod/master/pic/main.png "主界面")
* 参数设置  
![](https://raw.githubusercontent.com/sakuyaa/myNewTabMod/master/pic/config.png "参数设置")
* 将参数存放在火狐preferences里面  
![](https://raw.githubusercontent.com/sakuyaa/myNewTabMod/master/pic/prefs.png "首选项")
* 储存的Bing壁纸  
![](https://raw.githubusercontent.com/sakuyaa/myNewTabMod/master/pic/bingImg.png "Bing图片")

## 尚未解决（能力有限…）
* ~~由于使用了css3 transform移动来使主界面居中（这样才能保证每行的宽度不超过最大宽度时，导航宽度会自动适应），导致导航右边框消失。同时，当拖动导航网址时，链接并不会出现在鼠标上，而是鼠标右侧~~ 已使用marginLeft替代transform使界面居中
* chrome页面似乎用不了localStorage？
* 加载天气网页缓慢时会影响主页面的加载
