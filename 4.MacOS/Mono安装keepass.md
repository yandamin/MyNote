# Mac 安装运行keepass2.x

## 使用Mono运行keepass2.x

**先说问题，使用Mono安装有中文汉化问题，目前本人没解决**

**说白了就是使用类似wine的工具，将exe文件在macos上运行。不推荐！！！**

> 安装参考文档1： https://keepass.info/download/p_macosx/  
> 安装参考文档2：https://keepass.info/help/v2/setup.html#mono

1. ### 环境搭建

1. Install Mono ≥ 3.0 (http://www.mono-project.com/). # 先下载 Mono，（Mono就是一个在mac上运行windows应用的程序）
2. Install XQuartz ≥ 2.7.4 (https://www.xquartz.org/). # XQuartz 类似脚本执行命令的工具
下载下软件一路next 就行了。

3. Download one of the KeePass application ZIP packages above ..... # 注意不要在本页面下载 KeePass2.23.zip，这个没有解压没有 .exe文件
4. keepass2.x 下载地址：https://keepass.info/download.html，注意下载2.*.zip 免安装的版本。
5. 准备运行....

```
Other Unix-like systems:
In order to run KeePass, follow these steps:
    Install Mono ≥ 2.6 (older versions will not work and are not supported). Depending on your platform, the packages to install are called mono-stable, MonoFramework, mono-devel or mono-2.0-devel; see the Mono project page, if you are unsure which packages to install.
    On some platforms, the Windows Forms implementation (System.Windows.Forms) is offered as a separate package. KeePass requires this package; so if you see one, install it, too.
    On some platforms, the Runtime namespace (System.Runtime) is offered as a separate package. KeePass requires this package; so if you see one, install it, too.
    If you want to use auto-type on Linux / Mac OS X / BSD / etc., you additionally need the xdotool package.
    Download the portable version of KeePass (ZIP package) and unpack it to a location of your choice.
    When being in the KeePass directory, run the command line "mono KeePass.exe". Alternatively, right-click onto the KeePass.exe file, choose "Open with Other Application" and type in mono as custom command.
```

6. 解压keepass2.4.zip文件夹

![image-20191123122543752](https://tva1.sinaimg.cn/large/006y8mN6ly1g97v6moo2pj31440istlu.jpg)

7. `chmod +x /Users/yanmin/Downloads/KeePass-2.43/KeePass.exe` 注意权限问题。

8. 打开命令行，输入`mono32 /Users/yanmin/Downloads/KeePass-2.43/KeePass.exe` ，如果提示mono命令不认识，重新打开一个新的命令行执行。

9. 可能会提示mono32 需要安装下。

10. 如下图所示，可以使用了，但是中文是乱码的，进行了如下操作都没有生效。

    1. 设置了keepass软件字体：http://ju.outofmemory.cn/entry/371990
    2. 安装了中文字体：https://keepass.info/translations.html
    3. mono修改了配置文件字体

    ![image-20191123124421605](https://tva1.sinaimg.cn/large/006y8mN6ly1g97vhzxzgij30fq0l43zl.jpg)

11. XQuartz 怎么用？ 

    1. comand+ 空格，打开XQuartz ，在dock栏 XQuartz 图标上右键 - 应用程序 - 自定 - 添加项目
    2. 名称随便写，比如keepass
    3. 命令： `mono32 /Users/yanmin/Downloads/KeePass-2.43/KeePass.exe` 上一步启动keepass的命令
    4. 下次就可以快速启动了。