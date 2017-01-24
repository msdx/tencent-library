Tencent Library
===

用于将腾讯的一些公共第三方库打包为AAR并上传，以方便集成。
需要添加repository声明：
```gradle
    jcenter()
```

##CrashReport Upgrade
Bugly的升级包虽然出了aar包及依赖，但是里面并没有打包所需的AndroidManifest及其他资源文件，所以这里对其再次打包并发布。

Gradle 依赖：
```gradle
    compile 'com.githang:crashreport_upgrade:1.2.1'
```

注意：上面的依赖不包含nativecrashreport，如果需要，请添加以下依赖：
```gradle
    compile 'com.tencent.bugly:nativecrashreport:3.1.0'
```
