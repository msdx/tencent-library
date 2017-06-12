Tencent Library
====

Library|Latest Version
:---:|:---:
CrashReport| [ ![Download](https://api.bintray.com/packages/msdx/maven/CrashReport/images/download.svg) ](https://bintray.com/msdx/maven/CrashReport/_latestVersion) 
CrashReport Upgrade| [ ![Download](https://api.bintray.com/packages/msdx/maven/CrashReport_Upgrade/images/download.svg) ](https://bintray.com/msdx/maven/CrashReport_Upgrade/_latestVersion) 
TBS| [ ![Download](https://api.bintray.com/packages/msdx/maven/TBS/images/download.svg) ](https://bintray.com/msdx/maven/TBS/_latestVersion) 
Mid| [ ![Download](https://api.bintray.com/packages/msdx/maven/Tencent-Mid/images/download.svg) ](https://bintray.com/msdx/maven/Tencent-Mid/_latestVersion) 

----

用于将腾讯的一些公共第三方库打包为AAR并上传，以方便集成。
需要添加repository声明：
```gradle
    jcenter()
    maven { url 'https://dl.bintray.com/msdx/maven'} // use this if the artifact wasn't included in jcenter.
```

## CrashReport
Bugly的升级包虽然出了aar包及依赖，但是里面并没有打包所需的AndroidManifest及其他资源文件，所以这里对其再次打包并发布。

Gradle 依赖：
```gradle
    compile 'com.githang.tencent:crashreport:2.4.0'
```

注意：上面的依赖不包含nativecrashreport，如果需要，请添加以下依赖：
```gradle
    compile 'com.tencent.bugly:nativecrashreport:3.1.2'
```

## CrashReport Upgrade
Bugly的升级包虽然出了aar包及依赖，但是里面并没有打包所需的AndroidManifest及其他资源文件，所以这里对其再次打包并发布。

Gradle 依赖：
```gradle
    compile 'com.githang.tencent:crashreport_upgrade:1.2.1'
```

注意：上面的依赖不包含nativecrashreport，如果需要，请添加以下依赖：
```gradle
    compile 'com.tencent.bugly:nativecrashreport:3.1.0'
```

## TBS x5内核

```gradle
    compile 'com.githang.tencent:tbs:3.0.0.1038'
```

## Mid

Gradle 依赖：
```groovy
compile 'com.githang.tencent:mid:3.71'
```
