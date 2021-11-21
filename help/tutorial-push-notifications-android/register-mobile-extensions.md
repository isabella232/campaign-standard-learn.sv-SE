---
title: Steg 3 – registrera tillägg i din mobilapp
description: I den här delen ska vi lägga till koden för att registrera tilläggen UserProfile, Identity, Lifecycle och Signal.
feature: Push
kt: 4827
doc-type: tutorial
activity: use
team: TM
exl-id: d8c0d8c6-2e04-4c27-b27a-d0de79dd953b
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 11%

---

# Steg 3 – registrera tillägg i din mobilapp

I den här delen ska vi lägga till koden för att registrera tilläggen Användarprofil, Identitet, Livscykel och Signal. Dessa tillägg ingår i [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). Vi måste också registrera Adobe Campaign Standard-tillägget enligt koden nedan.

Öppna projektet i [!DNL Android] studio. Ta bort hela koden i MainApp **förutom den första raden som är programsatsen package**.

Klistra in följande kod i MainApp

<!--
Removed `{.line-numbers}` below
-->

```java
import [!DNL android].app.Application;
import android.util.Log;

import com.adobe.marketing.mobile.AdobeCallback;
import com.adobe.marketing.mobile.Campaign;
import com.adobe.marketing.mobile.Identity;
import com.adobe.marketing.mobile.InvalidInitException;
import com.adobe.marketing.mobile.Lifecycle;
import com.adobe.marketing.mobile.LoggingMode;
import com.adobe.marketing.mobile.MobileCore;
import com.adobe.marketing.mobile.Signal;
import com.adobe.marketing.mobile.UserProfile;

public class MainApp extends Application {

@Override
public void onCreate() {
super.onCreate();

MobileCore.setApplication(this);
MobileCore.setLogLevel(LoggingMode.DEBUG);

try{
    Campaign.registerExtension();
    UserProfile.registerExtension();
    Identity.registerExtension();
    Lifecycle.registerExtension();
    Signal.registerExtension();
    MobileCore.start(new AdobeCallback () {
        @Override
        public void call(Object o) {
            MobileCore.configureWithAppID("copy your launch property id here");
        }
    });
} catch (InvalidInitException e) {
    Log.d("ACS Exception", "exception");
}
}
}
```

Rad 32: du måste ange[!UICONTROL  Launch] Egenskapens miljöfil-ID. Du kommer åt detta via [!UICONTROL environment tab] på [!UICONTROL Launch] -egenskap.

![launch-id](assets/launch-id-property.PNG)
