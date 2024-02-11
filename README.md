# 基于FunDex2实现云脱壳

使用了lsp魔改全局版+fundex2实现云脱壳原理
测试环境

系统版本：Android10

FunDex2版本：720-7.2.0

LSPosed版本

LSPosed-v1.8.6-XiaoYing-Zygisk-Beta-1.0.15-6721-zygisk-release.zip

### 插件和adb环境下载

> FunDex2：[https://github.com/Xposed-Modules-Repo/com.zhenxi.fundex2](`https://github.com/Xposed-Modules-Repo/com.zhenxi.fundex2`)

> adb环境下载
> [platform-tools](https://developer.android.com/tools/releases/platform-tools)

没有adb环境需要自己下载安装，可自行搜索相关配置或者代码中指定adb.exe

#### zip内容说明

- apk -上传apk存放目录
- dex - 脱壳成功dex保存的目录
- main.py - 可以修改路径 端口号
- tk.py - 使用adb运行fundex2脱壳
- web.html - web
- ZhenxiConfig.xml - fundex2配置文件不需要修改
- 

### 说明

tk.py中

```
`phone_path = '/data/misc/8217b408-39a2-4489-a70e-04e78bea2811/prefs/com.zhenxi.FunDex2/'
```
![image](https://github.com/Zero1yi/fundex2-cloud-unpacker/blob/main/img/2.png)
8217b408-39a2-4489-a70e-04e78bea2811需要修改成自己的，使用魔改版
lsp激活插件到/data/misc/即可看到类型的目录
插件需要开启黑名单模式
该py脚本只是示范该插件云脱壳的原理。其他东西自己参考修改添加
运行main.py后，可浏览器打开[`http://127.0.0.1:1000/`](http://127.0.0.1:1000/)运行测试

默认端口情况下

![image](https://github.com/Zero1yi/fundex2-cloud-unpacker/blob/main/img/1.png)

代码使用了ai进行注解

上传格式 包名.apk 其他方式实现需要自己修改

![image](https://github.com/Zero1yi/fundex2-cloud-unpacker/blob/main/img/3.png)

tk.py中time.sleep(60)我不知道他是否有结束标志经过测试基本60s都可以完成(和手机性能有关系）具体自己修改或者研究一下

![image](https://github.com/Zero1yi/fundex2-cloud-unpacker/blob/main/img/4.png)
