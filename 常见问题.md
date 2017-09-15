#### WPS

##### 1.无法调用fcitx
~~~
在～/.profile中添加
export XIM="fcitx"
export XIM_PROGRAM="fcitx"
export XMODIFIERS="@im=fcitx"
export GTK_IM_MODULE="fcitx"
export QT_IM_MODULE="fcitx"
~~~

##### 2.word,excel,ppt无法输入中文
~~~
vim /usr/bin/wps
在第一行 #!/bin/bash下添加下面两行代码
export XMODIFIERS="@im=fcitx"
export QT_IM_MODULE="fcitx
ppt、excel和word一样添加环境变量，只是编辑的文件各不同
$ vi /usr/bin/wpp
$ vi /usr/bin/et
~~~

#### 常见问题
##### 1.桌面解压zip压缩文件为乱码
~~~
unzip -O CP936 xxx.zip
~~~

##### 2.fcitx无法开机自启动
~~~
目前fcitx启动文件所在路径:/usr/share/applications/fcitx.desktop
此文件拷贝到:~/.config/autostart/
如果没有autostart目录新建即可
~~~

##### 3.查看某个目录已经占用多少空间
~~~
du /home/bush/ExternalWebs　--max-depth=1 -h
~~~

##### 4.行首添加或者删除注释
~~~
添加
ctrl+v 进入列编辑模式,向下或向上移动光标,把需要注释的行的开头标记起来,然后按大写的I,再插入注释符,比如”#”,
再按Esc,就会全部注释了删除
先按v,进入visual模式,横向选中列的个数(如”#”注释符号,需要选中首列),再按Esc,再按ctrl+v 进入列编辑模式,
向下或向上移动光标,选中注释部分,然后按d, 就会删除注释符号()
~~~
