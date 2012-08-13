先是把全局的 graphics system 换成了 raster，结果是灾难性的，log in 后只能打开dolphin 和 yakuake。 手动把 `~/.kde4/env` 里的 `qt-graphicssystem.sh` 删了，重启，才恢复正常。

后来改 `/usr/share/autostart` 里的plasma-desktop.desktop, 和 `/usr/share/application` 里的 yakuake.desktop 加上`--graphicssystem raster` 的启动选项，目前感受上的确更流畅了，cpu 占用率也有显著降低。

ps.说到cpu，flashplayer11还真的是改善蛮大的。

