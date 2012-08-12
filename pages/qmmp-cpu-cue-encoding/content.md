# qmmp cpu 占用与.cue 转码

## qmmp cpu
调教前，播放时 cpu 占用60%~80%,暂停时在10%上下。

具体操作：
- 在 src 插件的参数设置中选线性插入。
- 在 `/usr/share/applications/qmmp.desktop` 中的 Exec 项中写入 `export QT_NO_GLIB=1;qmmp %F`

现播放时 cpu 占用 稳定10%以下。

## 转码 .cue 的 python 脚本
闲着没事写了一个，初步测试能用。
```python
#!/usr/bin/python
# Filename newconvert.py

import os
import fnmatch

cuepath = raw_input('The path where the \'.cue\' files are:')
incode = raw_input('Original encoding:')
outcode = raw_input('Output encoding:')
for root, dirs, files in os.walk(cuepath):
    print 'Working in %s.' % root
    for file in files:
        if fnmatch.fnmatch(file, '*.cue'):
            full_file_path = os.join.path(root,file)
            command = 'iconv -f %s -t %s -cs %s > %s' %(incode,outcode,full_file_path,full_file_path)
            try:
                os.system(command)
                print 'Converted %s' % file
            except OSError: 
                print 'Oops, Permission denied for %s' % file
            else :
                print 'Something went wrong and I have no idea why'
```
