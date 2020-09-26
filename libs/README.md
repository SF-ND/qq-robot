# cqhttp-mirai

这是[cqhttp-mirai](https://github.com/yyuueexxiinngg/cqhttp-mirai)的核心程序。

使用了[cqhttp-mirai-embedded](https://github.com/yyuueexxiinngg/cqhttp-mirai/tree/embedded)（这是内置了`Core`和`Console`的版本），相关配置方法可参考原仓库。

如果使用非`embedded`版本进行配置，需要注意`cqhttp`适配的是较老的`mirai`版本号，新版本不兼容。

## tips

可根据需要对`plugins`文件夹中的`setting.yml`进行配置。

运行`mirai-start.sh`即可启动程序，QQ账号密码在此文件中更改，可以配合`nohup`或是`screen`放到后台。