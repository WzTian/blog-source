# arch netcat slimv mit-scheme

slimv 的 mit-scheme支持要用到netcat的bsd版本，而arch里netcat-openbsd
这个包，安装之后生成的二进制文件名是nc.openbsd,因此要修改 `~/.vim/slime/contrib/swank-mit-scheme.scm`
的116行为 `(cmd (format #f "exec nc.openbsd -v -q 0 -l ~a 2>&1" port))`
