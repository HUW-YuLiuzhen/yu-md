# [IDEA安装和破解](http://www.itmind.net/16420.html)

## 一、安装

## 1. 下载安装包

我们先从 IDEA 官网下载 IDEA 2022.1 版本的安装包，下载链接如下：

https://www.jetbrains.com/idea/download/

IDEA插件：https://plugins.jetbrains.com/idea

![img](http://www.itmind.net/wp-content/uploads/2022/05/1651843669-175aeba83b608e3-1024x483.png)

 

## 2. 卸载老版本的 IDEA，并安装最新版本！

注意，如果电脑上之前有安装老版本的 IDEA, 需要先卸载干净，否则可能安装失败！

如果下载ZIP版本的话，直接解压即可。(建议直接下载zip版本)

如果下载了安装版本的话，需要正常安装即可！

此处就不多说了！

 

笔者下载了ZIP版本，解压ZIP文件之后可以看到bin目录下的文件

![img](http://www.itmind.net/wp-content/uploads/2022/05/1651844081-175aeba83b608e3.jpg)

点击idea64.exe 即可启动IDEA.

IDEA 运行成功后，会弹出下面的对话框，提示我们需要先登录 JetBrains 账户才能使用：

此时**直接退出**即可。不需要任何操作！

此时**直接退出**即可。不需要任何操作！

此时**直接退出**即可。不需要任何操作！

![IDEA 2022.1 弹出对话框，提示需要登录账户](http://www.itmind.net/wp-content/uploads/2022/08/20220813155156-1b4e5.png)

此时**直接退出**即可。不需要任何操作！

## 二、破解

http://www.itmind.net/16420.html

## 1、下载**破解补丁，然后解压**，打开文件夹如下：

### **注意：激活脚本获取方式如下：**

**关注公众号：Java技术指北 回复：\**dddd119\**，即可获取破解文件！**

![img](http://www.itmind.net/wp-content/uploads/2022/05/1651844244-175aeba83b608e3.png)

 

**注意：激活脚本文末获取！**

可以看到，相比较激活补丁之前的版本，新版本补丁z大新加了两个文件夹：

- scripts: 放置了相关脚本，包含自动安装、卸载破解补丁脚本（Windows、Mac、Linux 对应系统的脚本都有）；
  之前的 IDEA 版本，我们都是手动在 idea.vmoptions 配置文件引入破解补丁，但是有部分小伙伴反映找不到 idea.vmoptions 文件，这次，通过运行脚本可以直接引入补丁，针对小白，方便了很多。
- vmoptions： 放置了 JetBrains 产品的 idea.vmoptions 配置文件。之前版本都是通过在这个文件中手动引入破解补丁，但是最新版本 IDEA 2022.1 官方加入了反制手段，在用户目录下已经找不到这个文件了，新版本我们直接引用这个文件夹下的 idea.vmoptions 配置文件；

## 2、将 ja-netfilter-all激活文件夹移动到电脑上某个位置 并 运行激活脚本

**将 ja-netfilter-all激活文件夹移动到电脑上某个位置（注意不要使用中文路径）**，笔者做演示放置在了D盘里面，你也可以放到其他路径下：

![img](http://www.itmind.net/wp-content/uploads/2022/05/1651844486-175aeba83b608e3.png)

## 3、**点击运行 install-current-user.vbs 脚本，为当前用户安装破解补丁。**

Windows 系统，**点击运行 install-current-user.vbs 脚本**，为当前用户安装破解补丁。

Mac/Linux 系统，点击运行 install.sh 脚本安装。
PS: install-all-users.vbs 为系统所有用户安装，不太推荐。unistall-*前缀的是卸载补丁脚本。
点击安装，会弹出如下提示：

![安装IDEA激活破解补丁提示框](http://www.itmind.net/wp-content/uploads/2022/08/20220813155158-c533c.png)

告诉我们，运行此补丁大约花费几秒钟，点击 确定，等待 Done 完成提示框出现，到这里，表示补丁安装成功。

![IDEA 激活破解补丁安装成功](http://www.itmind.net/wp-content/uploads/2022/08/20220813155159-26765.png)
注意：运行此脚本因为需要添加 idea.vmoptions 文件的环境变量，可能会被杀毒软件误报为木马，大家允许运行即可。

实在不放心的小伙伴也可打开该脚本，看看源码，截图如下：

注意：运行此脚本因为需要添加 idea.vmoptions 文件的环境变量，可能会被杀毒软件误报为木马，大家允许运行即可。

实在不放心的小伙伴也可打开该脚本，看看源码，截图如下：

![IDEA 破解激活补丁源码截图](http://www.itmind.net/wp-content/uploads/2022/08/20220813155200-7fe90.png)

大致看下，代码主要是为 JetBrains 系列产品在外置 .vmoptions 配置文件中引用破解补丁：

![运行脚本自动引入了 IDEA 2022.1 的破解补丁](http://www.itmind.net/wp-content/uploads/2022/08/20220813155201-c8cd8.png)

以及添加idea.vmoptions 文件的环境变量，脚本运行成功后，打开环境变量看下，如下：

![img](http://www.itmind.net/wp-content/uploads/2022/05/1651844651-175aeba83b608e3.png)

可以看到，除了为 IDEA 添加 .vmoptions 环境变量外，还有其他产品的，如 Goland 等。

所以，小伙伴们不用担心是木马啥的，安心运行等待安装成功就行。

 

## 4.打开 IDEA, 填入指定激活码完成激活，然后重启**IDEA** 即可

运行脚本安装破解补丁完成后，**一定要重启 IDEA**，然后，填入下面的激活码，点击激活即可。

4W9NP3KV9E-eyJsaWNlbnNlSWQiOiI0VzlOUDNLVjlFIiwibGljZW5zZWVOYW1lIjoic2NyaXAgd2FuZSIsImFzc2lnbmVlTmFtZSI6IiIsImFzc2lnbmVlRW1haWwiOiIiLCJsaWNlbnNlUmVzdHJpY3Rpb24iOiIiLCJjaGVja0NvbmN1cnJlbnRVc2UiOmZhbHNlLCJwcm9kdWN0cyI6W3siY29kZSI6IklJIiwiZmFsbGJhY2tEYXRlIjoiMjAyMy0wMS0yNCIsInBhaWRVcFRvIjoiMjAyMy0wMS0yNCIsImV4dGVuZGVkIjpmYWxzZX0seyJjb2RlIjoiUERCIiwiZmFsbGJhY2tEYXRlIjoiMjAyMy0wMS0yNCIsInBhaWRVcFRvIjoiMjAyMy0wMS0yNCIsImV4dGVuZGVkIjp0cnVlfSx7ImNvZGUiOiJQV1MiLCJmYWxsYmFja0RhdGUiOiIyMDIzLTAxLTI0IiwicGFpZFVwVG8iOiIyMDIzLTAxLTI0IiwiZXh0ZW5kZWQiOnRydWV9LHsiY29kZSI6IlBHTyIsImZhbGxiYWNrRGF0ZSI6IjIwMjMtMDEtMjQiLCJwYWlkVXBUbyI6IjIwMjMtMDEtMjQiLCJleHRlbmRlZCI6dHJ1ZX0seyJjb2RlIjoiUFBTIiwiZmFsbGJhY2tEYXRlIjoiMjAyMy0wMS0yNCIsInBhaWRVcFRvIjoiMjAyMy0wMS0yNCIsImV4dGVuZGVkIjp0cnVlfSx7ImNvZGUiOiJQUEMiLCJmYWxsYmFja0RhdGUiOiIyMDIzLTAxLTI0IiwicGFpZFVwVG8iOiIyMDIzLTAxLTI0IiwiZXh0ZW5kZWQiOnRydWV9LHsiY29kZSI6IlBSQiIsImZhbGxiYWNrRGF0ZSI6IjIwMjMtMDEtMjQiLCJwYWlkVXBUbyI6IjIwMjMtMDEtMjQiLCJleHRlbmRlZCI6dHJ1ZX0seyJjb2RlIjoiUFNXIiwiZmFsbGJhY2tEYXRlIjoiMjAyMy0wMS0yNCIsInBhaWRVcFRvIjoiMjAyMy0wMS0yNCIsImV4dGVuZGVkIjp0cnVlfSx7ImNvZGUiOiJQU0kiLCJmYWxsYmFja0RhdGUiOiIyMDIzLTAxLTI0IiwicGFpZFVwVG8iOiIyMDIzLTAxLTI0IiwiZXh0ZW5kZWQiOnRydWV9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

复制激活码后填入，点击 Activate 按钮完成激活：

![填入 IDEA 2022.1 激活码](http://www.itmind.net/wp-content/uploads/2022/08/20220813155203-b96af.png)

 

点击激活后，就可以看到激活成功辣，

![img](http://www.itmind.net/wp-content/uploads/2022/05/1651844715-175aeba83b608e3.jpg)

 