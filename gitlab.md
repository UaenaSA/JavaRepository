# 搭建gitlab服务器 #

## 1.打开win功能 将.NET 3.5和4.7全部勾上![](https://i.imgur.com/dMp6N71.png) ##
## 2.下载BONOBO GIT SERVER，[http://bonobogitserver.com/](http://bonobogitserver.com/ "Bonobo.Git.Server") ##
## 3.解压后 目录结构如下 ![](https://i.imgur.com/cg4945J.png)##
## 4.打开控制面板-》系统和安全-》管理工具，点击Internet Information Services（IIS）管理器 ![](https://i.imgur.com/eg1yejC.png)##
## 5.添加网站![](https://i.imgur.com/spbJfLj.png)  ![](https://i.imgur.com/PktXfsC.png)##
## 6.配置应用程序池 右击Git->高级设置![](https://i.imgur.com/NBZJuEw.png) ![](https://i.imgur.com/1u7YQ84.png)##
## 7.注册asp.net(若已注册忽略) 打开管理员CMD `C:/Windows/Microsoft.NET/Framework/v2.0.50727/aspnet_regiis -i`##
## 8.部署映象服务和管理工具 在管理员CMD中执行如下4条命令 ##
### dism /online /enable-feature /featurename:IIS-ISAPIFilter ###
### dism /online /enable-feature /featurename:IIS-ISAPIExtensions###
### dism /online /enable-feature /featurename:IIS-NetFxExtensibility45###
### dism /online /enable-feature /featurename:IIS-ASPNET45###
## 9.打开配置文件 在如图所示的地方插入 `<validation validateIntegratedModeConfiguration="false"/>` ![](https://i.imgur.com/kFJv5tm.png)  ![](https://i.imgur.com/pwl3TW9.png)##
## 10.访问http://localhost:8810(端口号之前配置是多少就是多少)  初始账号密码都是admin![](https://i.imgur.com/NpetKpV.png)##
## 11.点击登录 进入到主页面 ![](https://i.imgur.com/DiDse43.png)##


