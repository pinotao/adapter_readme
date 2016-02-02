# 环境报错

* **Configuration with name 'debug' not found** 
    ![Configuration with name 'debug' not found ](http://cl.ly/2l3o0f2B3R2a/error1.png) 

    一般是clone完工程后，处在master分支，进行Gradle Sync操作，出现的报错提示。**解决方案**：checkout到开发分支，再同步。
    >有时候发现分支只有master且通过VCS的pull操作也无法更新到其他分支信息或者提示错误。这里可能是studio的问题，改用git命令行操作:git pull，即可更新到分支信息。
* **Configuration with name 'default' not found **
    ![Configuration with name 'default' not found ](http://cl.ly/0811450L0d0U/error2.png) 

    一般是clone完工程后，当前project存在其他依赖库或者module没有导入。**解决方案**：将未导入的module或者库添加后，再同步。
* **Error:SSL peer shut down incorrectly**
    ![Error:SSL peer shut down incorrectly ](http://cl.ly/073y2M2H091I/error3.png) 

    网络被天朝墙了：1.使用VPN代理。2.一般是指定的gradle版本，指定路径不存在，进入设置，设置使用本地的gradle版本，以及开启offline-work选项。
* **Build Tools 错误**
    ![Error:SSL peer shut down incorrectly ](http://cl.ly/030w2C040719/error4.png) 

    右键点击项目，选择“Open Module Settings”,切换本地存在的Build Tools Version 版本（或者直接在build.gradle脚本中修改
    >studio 2.0预览版7 之后，会直接有窗口提示是否下载指定的Build Tools Version。之前的版本可以自行打开SDK Manager 去下载指定版本。