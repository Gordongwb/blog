+++
title = "Arch linux 无法启动 chrome 的解决方法"
date = "2019-02-17T11:47:03+08:00"
draft = true
toc = true
summary = "我在arch上安装chrome之后，总是无法启动它，具体表现为任务栏上加载一段时间之后不弹出chrome窗口,查找资料后解决，方法如下"
tags= ["ArchLinux"]
categories= ["problems"]
+++

修改 /opt/google/chrome/google-chrome
在文件最后的 `exec -a "$0" "$HERE/chrome" "$@" --user-data-dir` 后加上`--no-sandbox`,然后保存退出即可。
