-- 环境配置 --------------------------------------------------------------------

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

2 问题2 Cordova及相关插件版本问题 注意版本兼容 比如 Cordova 几点几只能兼容androd几点几 见官网
3 下载模拟器及相关操作 Genymotion 见  https://www.cnblogs.com/rainboy2010/p/6387770.html  
4 如果提示 需要安装  
```
Discovered plugin "cordova-plugin-whitelist" in config.xml. Adding it to the project
Fetching plugin "cordova-plugin-whitelist@1" via npm
Installing "cordova-plugin-whitelist" for android

```
解决办法 安装 npm install cordova-plugin-whitelist  

# cordova 插件大全
https://www.jianshu.com/p/642c9be55446?utm_campaign=maleskine&utm_content=note&utm_medium=seo_notes&utm_source=recommendation

-- 遇到的坑 --------------------------------------------------------------------

# 打包后js无效 （坑）
比如绑定按钮点击事件无效  
原因：
1 html中元素放在div class =“app"元素内  
2 js事件绑定在index.js中的onDeviceReady中绑定。

# Cordova - 打包Vue项目的详细步骤（将Vue.js项目编译成App）
http://www.hangge.com/blog/cache/detail_2101.html

# Cordova多页面应用 可以a标签链接跳转配置
见 https://stackoverflow.com/questions/36036475/cordova-6-0-ios-load-external-url-in-the-webview

删除这两行  添加一行   
```
<allow-intent href="http://*/*" /> // 删除
<allow-intent href="https://*/*" />  // 删除 
```
添加这一行
```
<allow-navigation href="*" />
```

# Cordova Ajax请求跨域问题整理
