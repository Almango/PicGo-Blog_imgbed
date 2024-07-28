## 搭建教程
### 安装PicGo
>PicGo 是一个用于快速上传图片并获取图片 URL 的工具，它支持多种图床服务，如 GitHub、阿里云 OSS、腾讯云 COS 等。通过 PicGo，用户可以方便地将图片上传到指定的图床，并获取到图片的链接，用于在网页、博客或其他文档中展示图片。

1 . 需要先下载并安装PicGo。

**官网地址**：[https://picgo.github.io/PicGo-Doc/zh/](https://picgo.github.io/PicGo-Doc/zh/)


### 创建Github仓库
> 创建一个仓库用作图床的储存库

1 . 创建完成成后，打开gihub的设置选项：`Settings`.

2 . 在侧边栏点击：`Developer settings`。

3 . 将`Personal access tokens` 展开，并点击`Tokens (Classic)`，新建一个tokens，自定义一个秘钥并确认。


![](https://cdn.jsdelivr.net/gh/Almango/Blog_imgbed@main/post/post_picgo_1.png)

4 . 新建秘钥后，将秘钥复制下来。

### 配置PicGo

1 . 启动PicGo。
2 . 在侧边栏，将`图床设置`展开，点击Github项。
3 . 在设置选项中：
 - 设置仓库名：用户名/仓库名
 - 设定分支名：分支名（main / master）
 - 设定Token：Github创建的秘钥
 - 设定存储路径：仓库里的子目录名称（可选）
 - 设定自定义域名：https://cdn.jsdelivr.net/gh/[用户名]/[仓库名]@main


![](https://cdn.jsdelivr.net/gh/Almango/Blog_imgbed@main/post/post_picgo_2.png)

4 . 到这里，PicGo已经配置完成。

5 . 可以正常上传图片。

### 说明

1 . Github被当做图床的储存仓库，通过Token将仓库和PicGo连接起来，可以在PicGo中快速的向仓库中上传图片。

2 . 为了防止Github被DNS污染，这里使用JSDliver来解决此问题。
>sDelivr是一个免费开源的CDN解决方案，用于帮助开发者和站长。 包含 JavaScript 库、jQuery 插件、CSS 框架、字体等等 Web 上常用的静态资源。

3 . 虽然起到CDN加速作用，但效果并不显著，如果有条件可以购买更好的CDN加速。

4 . 以上就是对整个图床的搭建及其大概说明。

