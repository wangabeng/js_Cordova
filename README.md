# js_Cordova
hybird混合app

# Cordova环境配置
详细配置教程 https://blog.csdn.net/zsion409540923/article/details/78811054#%E7%AC%AC%E4%BA%94%E6%AD%A5%E5%AE%89%E8%A3%85gradle  

安装问题解决：
见 https://blog.csdn.net/kongxx/article/details/78156490?utm_source=tuicool&utm_medium=referral  
1 问题1 Failed to find 'ANDROID_HOME' environment variable 没有配置好ANDROID环境变量  
解决办法  
```
配置Andriod环境变量前提是要先安装好JAVA环境

1、下载Android SDK，点击安装，直接默认路径即可！ 下载地址：http://developer.android.com/sdk/index.html

2、默认路径安装后，安装完成，开始配置环境变量。

3、打开计算机属性——高级系统设置——环境变量（如上文）

4、新建一个环境变量，变量名：ANDROID_HOME，变量值：D:\adt-bundle-windows-x86_64-20140702\sdk（以你安装目录为准,确认里面有tools和add-ons等多个文件夹），点击确认。

5、在用户变量PATH后面加上变量值;%ANDROID_HOME%\platform-tools;点击确认即可。 在系统变量path中添加;D:\adt-bundle-windows-x86_64-20140702\sdk\tools

6、Android SDK配置完成，接下来验证配置是否成功。

7、点击运行——输入cmd——回车——输入adb——回车，如果出现一堆英文，如下图所示，即表示配置成功，在输入Android，启动Android SDK Manager。
```

2 问题2 提示 Could not find an installed version of Gradle either in Android Studio  
