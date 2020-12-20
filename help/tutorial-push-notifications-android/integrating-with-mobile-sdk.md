---
title: Steg 2 – integrera en mobil SDK
description: I den här delen integrerar vi Android-appen med Mobile SDK. Integrera mobil-SDK med Android-appen
feature: Push
topics: Mobile
kt: 4826
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 13b4f1d395dfe53f9fc5263e7b06be700e30b986
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 3%

---

# STEG 2 - Integrera [!UICONTROL Mobile SDK] med Android-app

I den här delen integrerar vi [!DNL Android]-appen med [!UICONTROL Mobile SDK]. Följ de här stegen för att integrera [!UICONTROL mobile SDK] med [!DNL Android]-appen:

* Öppna *ACSPushTutorial*-projektet i [!DNL Android Studio]
* Skapa en ny java-klass med namnet *MainApp* som utökar [!DNL android.app.Application]
* Projektstrukturen bör nu se ut så här

![huvudprogram](assets/android-main-app.PNG)

* Expandera mappen [!DNL Gradle Scripts]. Dubbelklicka på [!DNL build.gradle] i modulen. Klistra in följande beroenden i avsnittet om beroenden i filen [!DNL build.gradle]. Din [!DNL build.gradle]-fil ska nu se ut så här

<!--
Removed `{.line-numbers}` below
-->

```java
implementation 'com.adobe.marketing.mobile:campaign:1.+'
implementation 'com.adobe.marketing.mobile:userprofile:1.+'
implementation 'com.adobe.marketing.mobile:sdk-core:1.+'
```

![modul-gradle](assets/module-build-gradle.PNG)

* Synkronisera ditt [!DNL Android]-projekt genom att klicka på knappen Synkronisera nu för att synkronisera projektet

## Ändra [!DNL AndroidManifest.xml]{#modify-android-manifest}

Öppna *AndroidManifest.xml* och klistra in följande två rader efter manifest-elementet och före application-elementet. Detta gör att appen kan kommunicera med andra användare

<!--
Removed `{.line-numbers}` below
-->

```xml
<uses-permission android:name="android.permission.INTERNET" />
<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />
```

Kopiera följande rad i elementet application
[!DNL android:name=".MainApp"]
Spara din [!DNL AndroidManifest.xml]
Din [!DNL AndroidManifest.xml] ska se ut så här

<!--
Removed `{.line-numbers}` below
-->

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.example.acspushtutorial">
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.ACCESS_NETWORK_STATE" />

<application
    android:name=".MainApp"
    android:allowBackup="true"
    android:icon="@mipmap/ic_launcher"
    android:label="@string/app_name"
    android:roundIcon="@mipmap/ic_launcher_round"
    android:supportsRtl="true"
    android:theme="@style/AppTheme">

<activity android:name=".MainActivity">
<intent-filter>
    <action android:name="android.intent.action.MAIN" />
    <category android:name="android.intent.category.LAUNCHER" />
</intent-filter>
</activity>
</application>

</manifest>
```
