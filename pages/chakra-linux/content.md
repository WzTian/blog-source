# Chakra Linux 安装配置笔记

## 安装
Chakra 的Live cd 做的很不错。与实际安装速度上差距不大，在n卡机器上运行顺利，特效正常开启。
Tribe不比Anaconda在差，安装结束后提示安装常用bundle很贴心，
此外自动识别windows启动项也省去了我手动配置的工夫。整个过程不能再顺利了。

## 输入法
输入法用fcitx4,源里有scim，无ibus。firefox bundle中fcitx输入不能。据fcitx开发者@csslayer 说是
bundle自用的gtk与系统的im-xim.so不兼容。不得已编译了(也是@csslayer负责的）
firefox-kde-opensuse，编了两个小时，粉碎了我用Gentoo的一切幻想。
同是bundle gimp中fcitx表现良好。

## 字体
源里有文泉驿微米黑，作为系统字体中英文均胜任，不赘言。

## 活动/Activity
我觉得这个功能的心理意义大于实际意义，与虚拟桌面的区别无非就是切换不那么直观了，
但客观上的确起到了集中注意力的作用，等kde4.7发布实现活动与程序的绑定
后倒能算一个killer feature（其实我现在开机设置自动恢复上次会话，效果也差不多吧）。

## GTK 程序
装了好几个bundle，真正在用的只有gimp，播放器用qmmp代替了以前用的audacious，
ape+cue无压力。从ccr 里装了一个kmldonkey,还没用过，争取替代amule。

## 感觉
Chakra的kde调教的很细致，主题kneda很好不说，plasmoid种类较 **Fedora** 丰富，
显示天气的那个plasmoid 也不用我每次连wifi后都手动刷新了。
appset-qt很弱，但日常都用pacman,所以没什么关系。
总而言之，在我用过的发行版（Ubuntu,Fedora,Puppy,Chakra)中Chakra是我目前为止感觉最舒心的一个，
加之其采用滚动升级，我已有了长期坚守的打算。 



