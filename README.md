# QQ Artificial Idiot

> 基于`cqhttp-mirai`的QQ机器人

<div align="center">
   <img width="233" src="https://s1.ax1x.com/2020/09/26/0PtZCD.png" alt="logo"></br>
mirai 是一个在全平台下运行，提供 QQ Android 协议支持的高效率机器人库

这个项目的名字来源于
     <p><a href = "http://www.kyotoanimation.co.jp/">京都动画</a>作品<a href = "https://zh.moegirl.org/zh-hans/%E5%A2%83%E7%95%8C%E7%9A%84%E5%BD%BC%E6%96%B9">《境界的彼方》</a>的<a href = "https://zh.moegirl.org/zh-hans/%E6%A0%97%E5%B1%B1%E6%9C%AA%E6%9D%A5">栗山未来(Kuriyama <b>mirai</b>)</a></p>
     <p><a href = "https://www.crypton.co.jp/">CRYPTON</a>以<a href = "https://www.crypton.co.jp/miku_eng">初音未来</a>为代表的创作与活动<a href = "https://magicalmirai.com/2019/index_en.html">(Magical <b>mirai</b>)</a></p>
图标以及形象由画师<a href = "https://github.com/DazeCake">DazeCake</a>绘制
</div>

说明书可到[OneBot](https://github.com/emoust/onebot/blob/master/v11/specs/README.md)查看。

## 文件结构

* `libs`: `cqhttp-mirai`核心程序

## 故事

2019年的体育节，为了实现一个突然产生的QQ点歌想法，仅仅用了一个周末的亚子，基于[酷Q](https://github.com/richardchien/coolq-http-api)的QQ机器人就被搭建了起来。当时这玩意儿是用`docker`里的`wine`模拟`Tim`的解决方案，通过一个`Vnc`远程桌面即可操控。点歌接收程序用`Python`的网络编程草草写了一个出来，再配合`Mysql`、`PHP`和`HTML`进行审核、播放和歌曲展示。虽然中途也出现了一些技术问题上的小插曲，但直到结束，一共接收了近`1000`首歌，发送信息`5000`条左右。应该也算是很辉煌的战绩了吧。

后来，QQ机器人被配合用作「时光信笺」。

这个版本的QQ机器人除了手机无法同时登陆也没啥不好，有浏览器就可以进行简单的管理。然而2020年中寻，万恶的企鹅对QQ机器人进行了一波“焚书坑儒”，之前的解决方案失效了，正值师附学生组织架构重组，便也无心打理。

然鹅历史仍然在波浪式前进，螺旋式上升，一切有了新的开始，便也不想就此放弃。放眼望去，似乎[mirai](https://github.com/mamoe/mirai)是一个挺不错，而且几乎是唯一的选择。现在是高考听力前夜，终于把[cqhttp-mirai](https://github.com/yyuueexxiinngg/cqhttp-mirai)跑起来了。这玩意儿纯命令行操作，模拟了一个`aPad`设备，手机也可以同时登陆（这可实在是太香了）。

## 注意事项

**无法发送图片**
发现`su`账号发不了图片，发出去是加载不出来的，但是用另外一个账号发送同一张图片以后，原来加载不出来的图片就又可以了，又加载出来的原因应该是全局哈希，但是`su`为什么发送不了图片现在还不知道（或许是因为之前挂过机器人群发过所以被该死的企鹅关小黑屋了）。总之现在的解决方案就是后端得挂着两个号，发送图片的同时用另一个号给自己发送相同的图片，这样发送出去的图片就能顺利加载了。
