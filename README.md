# QQ机器人

## 故事

2019年的体育节，为了实现一个突然产生的qq点歌想法，仅仅用了一个周末的亚子，基于[酷Q](https://github.com/richardchien/coolq-http-api)的QQ机器人就被搭建了起来。当时这玩意儿是用`docker`里的`Wine`模拟`Tim`的解决方案，通过一个`Vnc`远程桌面即可操控。点歌接收程序用`Python`的网络编程草草写了一个出来，再配合`Mysql`、`PHP`和`HTML`进行审核、播放和歌曲展示。虽然中途也出现了一些技术问题上的小插曲，但直到结束，一共接收了近`1000`首歌，发送信息`5000`条左右。应该也算是很辉煌的战绩了吧。

后来，QQ机器人被配合用作「时光信笺」。

这个版本的QQ机器人除了手机无法同时登陆也没啥不好，有浏览器就可以进行简单的管理。然而2020年中寻，企鹅对qq机器人进行了一波“焚书坑儒”，之前的解决方案失效了，正值组织架构重组，便也无心打理。

然鹅历史仍然在波浪式前进，螺旋式上升，也不想就此放弃。放眼望去，似乎`mirai`是一个挺不错，而且几乎是唯一的选择。现在是高考听力前夜，终于把`cqhttp-mirai`跑起来了。这玩意儿纯命令行操作，模拟了一个`aPad`设备，手机也可以同时登陆（这可实在是太香了）。
