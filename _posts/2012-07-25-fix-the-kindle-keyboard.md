---
layout: post
title: "Fix the Kindle Keyboard"
description: ""
category: Digital Life
tags: [kindle]
---
{% include JB/setup %}

开头需要提一下，这是一篇拖了大概快2周的文章。

我的Kindle Keyboard自从6月中旬因为进程条卡在大树那里，之后被我自己的误操作格式化了所有的分区。

剩下Recovery Mode一个功能，这个应该是写在机身的内存上，所以我猜测硬件方面是没有问题，只是原生的Kindle系统和多看已经被我的误操作之后都格式化了，所以当时是启动不了系统的。

百度了一番后，发现我并不是第一个个例，以后手贱之前要把百度先翻了一遍，不然会死得很惨。

好在USB-TTL电平转换器到手后救活我的Kindle Keyboard。下面开始是我的一些心得。

修复好的前提是你必须有一个Linux，因为Kindle的650M系统分区只能在Linux下才能被识别。

至于Linux版本没有讲究，用到的软件是Minicom或者图形化的Cutecom。

所需要的命令和拆开Kindle后需要焊的TXD,RXD,GND位置见[链接](http://bbs.mydoo.cn/thread-33833-1-1.html)的详细介绍

有一点需要注意的是Kindle的TXD,RXD要和USB-TTL电平转换器的RXD,TXD对应，也就是反着来接。

我第一次尝试的时候就是没有反接，所以没有办法控制Kindle。

另外就是你需要准备好对应的rootfs.img恢复到分区，至于版本好像没有要求，只需要WIFI的kindle对应WIFI的rootfs.img就可以了，这个要大家自己尝试了。

另外还有第二张方法，不过只是不需要USB-TTL电平转换器而已，还是需要Linux的。

在完全关机的状态下按回车键15秒,等出现恢复菜单都按ALT+E。

密码数字部分采用ALT+QWERTYUIOP 对应1234567890。

密码输入完回车后再接USB,就能进650MB的分区恢复模式。

看Kindle恢复密码的[软件](http://www.siralex.info/2011/06/13/kindle-diagnostic-tool/)。

然后把准备好的rootfs.img恢复到相应的分区,命令参考[上文提到的那篇帖子](http://bbs.mydoo.cn/thread-33833-1-1.html)。

我用的是一位热心坛友提供的一个kindle WIFI B008版的img [下载链接](http://115.com/file/aq1er3h1)。

其他的版本请自行百度或者前往多看论坛搜索。