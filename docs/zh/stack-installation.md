# 初始化安装

在云服务器上部署 Seafile 预装包之后，请参考下面的步骤快速入门。

## 准备

1. 在云控制台获取您的 **服务器公网IP地址** 
2. 在云控制台安全组中，检查 **Inbound（入）规则** 下的 **TCP:80** 和 **TCP:9002** 端口是否开启
3. 若想用域名访问 Seafile，请先到 **域名控制台** 完成一个域名解析

> 9002 是用于文档预览和编辑的 OnlyOffice Document Server 服务所需的端口

## Seafile 安装向导

1. 使用本地电脑的 Chrome 或 Firefox 浏览器访问网址：*http://域名* 或 *http://公网IP*, 进入Seafile登录页面
   ![Seafile登录页面](http://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-login-websoft9.png)

2. 输入用户名和密码[（查看）](/zh/stack-accounts.md)，登录到Seafile后台管理界面
   ![Seafile后台界面](http://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-bk-websoft9.png)

3. 设置（检查） Seafile 的真实主机地址（**必选项，否则无法使用文件上传功能**）

   - SERVICE_URL：*http://服务器公网IP*
   - FILE_SERVER_ROOT：*http://服务器公网IP/seafhttp*

   ![Seafile后台界面](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-seturl-websoft9.png)


4. 开始使用 Seafile 全面友好的功能吧

> 需要了解更多Seafile的使用，请参考：[《Seafile 用户手册》](https://cloud.seafile.com/published/seafile-user-manual/home.md) 和 [《Seafile 服务器手册》](https://cloud.seafile.com/published/seafile-manual-cn/home.md)

5. 安装授权文件(仅支持seafile企业版)

   如果您已经向 Seafile 软件商购买了专业版的授权文件seafile-license.txt，您只需要将该授权文件拷贝至 Seafile 数据持久化目录中的/data/wwwroot/seafile/seafile-data/seafile/目录下，然后重启docker容器，即可完成授权文件的安装。
   
```bash
cp seafile-license.txt /data/wwwroot/seafile/seafile-data/seafile/
docker restart seafile
```
## Seafile 入门向导

Seafile 是一款开源的企业云盘，作为企业云盘，主要用于网络存储和管理文件，以及文件共享和协同办公。在使用 Seafile 时，有如下常规操作：

- 用户和分组管理，用于用户管理，和成员分组统一管理
- 文件和文件库管理，用于文件的管理和分类，并通过查看文件的历史信息了解文件的版本变更
- 共享与写作，用于将文件或文件库共享给个人或群组，实现协同办公

下面我们通过创建资料库、创建文件、编辑文件、设置权限、用户共享等操作，来熟悉 Seafile 的使用。

### 添加文件

下面我们介绍如何添加和编辑文件：

1. 登录到 Seafile 后，添加资料库，然后添加文件

   ![Seafile添加资料库](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-addlib-websoft9.png)

   ![Seafile添加文件](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-addfile-websoft9.png)

2. 在线编辑文件（通过内置的 OnlyOffice Document Server 服务实现）

   ![Seafile编辑文件](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-editfile1-websoft9.png)

### 用户管理

下面我们介绍如何创建用户和群组：

1. 打开右上角用户图标，进入【系统管理】，分别添加【用户】和【群组】

   ![Seafile进入系统管理](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-system-websoft9.png)

   ![Seafile添加用户](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-adduser-websoft9.png)

   ![Seafile添加群组](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-addgroup-websoft9.png)

2. 设置所创建的用户所归属群组

   ![Seafile用户分组](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-addusertogroup-websoft9.png)

### 文件共享

下面我们介绍如何给另外一个用户共享自己的文件：

1. 进入【我的资料库】，将资料库共享给指定用户，

   ![Seafile文件共享](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-sharefile1-websoft9.png)


2. 设定权限为【可写】或【只读】

   ![Seafile文件共享](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-sharefile-websoft9.png)

   > 在选择用户时，需输入用户名，系统自动查找匹配

### 读写共享文件

下面我们演示用户如何读写其他人共享过来的文件：

1. 切换user1用户登录，使用邮箱地址【user1@websoft9】作为登录名
   ![Seafile登录页面](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-login1-websoft9.png)

2. 查看共享文件，进入 OnlyOffice 进行编辑，保存文档
   ![Seafile查看共享文件](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-viewsharefile-websoft9.png)
   ![Seafile编辑共享文件](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-editfile-websoft9.png)

3. 切换到管理员账号 `me@example.com`，查看共享文件的版本变更信息
   ![查看共享文件版本信息](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-viewfileinfo1-websoft9.png)
   ![查看共享文件版本信息](https://libs.websoft9.com/Websoft9/DocsPicture/zh/seafile/seafile-viewfileinfo-websoft9.png)


## 常见问题

#### 浏览器打开IP地址，无法访问 Seafile（白屏没有结果）？

您的服务器对应的安全组80端口没有开启（入规则），导致浏览器无法访问到服务器的任何内容

#### 本部署包采用的哪个数据库来存储 Seafile 数据？

MariaDB/MySQL on Docker

#### 为什么使用 Docker 安装 Seafile？

是官方推荐的安装方式

#### 默认是否支持文档预览与编辑？

支持
