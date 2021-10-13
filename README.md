# AutoPermit
一款Android自动授予权限开源库，你只需要在Androidmanifest申请权限即可，然后在Activity中使用本插件即可。本插件的优点是，不需要你手动的去requestPermission各个动态权限，插件会帮你自动获取需要动态申请的权限。具体的使用如下：

## 依赖
在app.build中依赖
```java
maven{url 'https://gitee.com/haochen12/HowzitsMaven/raw/master'}
```
如下：
```java
   repositories {
        maven{url 'https://gitee.com/haochen12/HowzitsMaven/raw/master'}
    }
```
在build.gradle 中依赖：

```java
implementation 'com.howzits.autopermit:autopermit:0.0.1-SNAPSHOT'
```
## 手动授予权限

```java
AutoPermit.With(this)  
        .setAuto(false)  
        .setPermissions(new String[]{Manifest.permission.WRITE_EXTERNAL_STORAGE,  
                Manifest.permission.READ_CALENDAR,  
                Manifest.permission.READ_EXTERNAL_STORAGE}) 
        .setRequestCode(10)  
        .request();  
```
## 自动赋予权限  
```java
AutoPermit.With(this)  
        .setAuto(true)  //设置自动赋予权限
        .setRequestCode(10)  //设置requestcode
        .request();
```
  
