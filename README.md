# aliyundriver-webdav

# 好用请点个star吧



#### 软件说明: 本软件只是一个通过go的ui界面软件, 不涉及任何的阿里云盘数据, 方便设置,开机自启,操作控制的界面控制台的软件




#### 介绍

{**阿里云盘/本地挂载网络盘/WebDAV/win软件/界面**}

#### 软件架构

https://fyne.io/fyne/v2 v2.1.2 ui框架

https://github.com/getlantern/systray 任务栏(win10 bug不少 弃用)

https://github.com/gookit/goutil (工具类)

https://github.com/messense/aliyundrive-webdav (一个rust写的webdav)

ui框架加载失败的后补方案

https://cn.vuejs.org/index.html (vue.js)

https://jquery.com/ (jquery)

https://getbootstrap.com/ (bootstrap)



## 



#### 安装教程(界面存在一定偏差)

- 直接下载zip
- 下载阿里云盘webdav  https://github.com/messense/aliyundrive-webdav/releases, 将aliyundrive-webdav.exe放于 bin目录下
- 运行根目录下 aliyundriver-webdav.exe 即可启动服务

关于开机自启 需要RaiDrive 和 webdav服务开机自启, webdav设置自启可能需要管理员权限

仅校验过 阿里云盘webdav 1.1.0版本

#### 更新记录

-  如果启动失败,可以执行change_mode.exe切换至web模式



**遇到问题可以查看 常见为题, 使用过程中存在的问题和解决也可以反馈记录**



#### 使用说明

# 安装RaiDrive

文件在指南目录下, 你也可以自行下载

配置

**最简单只需要填 refreshToken( 建议改端口 防止被占用)**

`注意, 把地址Address去掉 不使用https`

![image-20220106211654620](README.assets/image-20220106211654620.png)





# 获取refreshToken

> **1. 登录阿里云**
>
> https://www.aliyundrive.com/
>
> 2. 浏览器打开**开发者模式(F12)**
>
> ![image-20220106211310171](README.assets/image-20220106211310171.png)
>
> 3. **获取refreshToken**
>    ![image-20220106211538483](README.assets/image-20220106211538483.png)

## 配置RaiDrive

`注意, 把地址Address去掉 不使用https`

![image-20220114092345822](README.assets/image-20220114092345822.png)

# 启动Raidrive服务

![image-20220107112639591](README.assets/image-20220107112639591.png)

# 查看是否生效

![image-20220107112534270](README.assets/image-20220107112534270.png)

# 没有生效

查看日志文件/logs(还没完善 有问题请联系)

# 常见问题

> refresh_token
>
> > 每次启动程序会刷新refresh_token, webdav启动的时候 refresh_token会刷新, 当前简单实现, 只在程序启动获取刷新后的refresh_tokenUI显示, 当自动刷新的refresh_token发生变更, 手填的会被覆盖
> >
> > refreshToken长度只有36位数字英文组成
>
> 关于程序启动问题
>
> > 管理员启动webdav程序, 需要管理权限关闭
> >
> > 设置开机自启需要使用管理员权限
> >
> > 启动webdav服务后可以退出本程序, 不需要一直启动
> >
> > 查看日志发现OpenGl不兼容, 可以执行change_mode.exe, 切换到web模式
>
> 程序配置
>
> > 红色必填
> >
> > 绿色建议
> >
> > 灰色可选
>
> 关于程序路径问题
>
> > 如果程序在C盘目录下, 开机自启有可能不成功
> >
> > 如果你设置了开机自启, 又移动了程序路径将不生效
>
> 关于程序下载
>
> > 建议直接把完整下载, 里面包含了字体文件等, 如果只下载exe存在乱码等情况
>
> 



#### 更新详情

- openGL不兼容解决方案

  > 因为fyne ui框架使用的openGL,如果启动失败可以web页面代替方案 如果启动失败,可以执行change_mode.exe切换至web模式
  >
  > 当**软件ui启动失败的时候,会启动web服务进行配置**,页面和软件配置基本一样
  >
  >
  > ![image-20220317190916915](README.assets/image-20220317190916915.png)







#### 参与贡献

1. Fork 本仓库
2. 新建 Feat_xxx 分支
3. 提交代码
4. 新建 Pull Request

5. https://gitee.com/gitee-stars/)

##免责声明

- 本软件为免费开源项目，无任何形式的盈利行为。
- 本软件服务于阿里云盘，旨在让阿里云盘功能更强大。如有侵权，请与我联系，会及时处理。
- 本软件仅软件壳子,核心服务调用aliyundrive-webdav (一个rust写的webdav)的做流量转发，不拦截、存储、篡改任何用户数据。
- 严禁使用本软件进行盈利、损坏官方、散落任何违法信息等行为。
- 本软件不作任何稳定性的承诺，如因使用本软件导致的文件丢失、文件破坏等意外情况，均与本软件无关。



## JetBrains 开源证书支持
感谢 JetBrains 提供的免费授权
![image](https://user-images.githubusercontent.com/41338363/170253261-67e7d599-f601-442b-b95e-4431ef151e7c.png)

