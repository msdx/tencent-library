Tencent Library
====

Library|Latest Version
:---:|:---:
CrashReport| [ ![Download](https://api.bintray.com/packages/msdx/maven/CrashReport/images/download.svg) ](https://bintray.com/msdx/maven/CrashReport/_latestVersion) 
CrashReport Upgrade| [ ![Download](https://api.bintray.com/packages/msdx/maven/CrashReport_Upgrade/images/download.svg) ](https://bintray.com/msdx/maven/CrashReport_Upgrade/_latestVersion) 
TBS| [ ![Download](https://api.bintray.com/packages/msdx/maven/TBS/images/download.svg) ](https://bintray.com/msdx/maven/TBS/_latestVersion) 
Mid| [ ![Download](https://api.bintray.com/packages/msdx/maven/Tencent-Mid/images/download.svg) ](https://bintray.com/msdx/maven/Tencent-Mid/_latestVersion) 
MTA| [ ![Download](https://api.bintray.com/packages/msdx/maven/Tencent-MTA/images/download.svg) ](https://bintray.com/msdx/maven/Tencent-MTA/_latestVersion) 

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
    compile 'com.githang.tencent:crashreport_upgrade:1.3.1'
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

AndroidManifest.xml
```xml
<!--MID3.5以上版本请务必添加此配置-->
    <provider
        android:name="com.tencent.mid.api.MidProvider"
        android:authorities="${applicationId}.TENCENT.MID.V3"
        android:exported="true" >
    </provider>
```

## MTA

so: arm64-v8a, armeabi, armeabi-v7a, mips, mips64, x86, x86_64

Gradle 依赖：
```groovy
compile 'com.githang.tencent:mta:3.1.0'
```

AndroidManifest.xml
```xml
    <provider
        android:name="com.tencent.mid.api.MidProvider"
        android:authorities="${applicationId}.TENCENT.MID.V3"
        android:exported="true" >
    </provider>
    <meta-data android:name="TA_APPKEY" android:value="ABCDEFG12233456"/>
    <!-- 请将value改为app发布对应的渠道，不同的发布渠道使用不同的名字 < -->
    <meta-data android:name="InstallChannel" android:value="play"/>
    <!-- 注意：若填写的渠道为纯数字字符串类型，请不要超过int表示的范围！ < -->
```