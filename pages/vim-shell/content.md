# 在vim里整合shell的小结

vim的开发者Bram Moolenaar明确的表示了不会在主线的vim里
整合shell，但这并不妨碍有志者进行拓展。

## python的!VimSh
http://www.vim.org/scripts/script.php?script_id=165

这个是我最先找到的，bash的确跑起来了，但prompt样式怪异，
`ls`之后目录显示也有问题，应该是色彩设置上不支持，用了一会
还有各种各样的问题，基本没有什么可用性。

## ConqueTerm

这个是Linux Toy上介绍的，今天试用了一会儿，觉得非常好用，反应速度也还好，
中文，色彩，一切正常。
`~./.vimrc`里加了一句：`map <leader>sh :ConqueTerm bash<cr>`

http://www.vim.org/scripts/script.php?script_id=2771

## Screen Shell

这个是之前一直用的，倒也蛮好，就是screen里面似乎不支持256色，molokai配色
没有了，于是果断抛弃。

http://www.vim.org/scripts/script.php?script_id=2711

其实`Ctrl-z`再`fg`也是不错的方式，但输入命令时看不了代码。
`:! some-command` 只是一次性的，略有不足。


