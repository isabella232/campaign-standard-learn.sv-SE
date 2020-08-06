---
title: Steg 3 - Registrera tillägg i din mobilapp
description: I den här delen ska vi lägga till koden för att registrera tilläggen UserProfile, Identity, Lifecycle och Signal.
feature: Push
topics: Mobile
kt: 4827
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: c3ff1a137fb8ee9506a11f82e1a27d010bbd97e6
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---


# Steg 3 - Registrera tillägg i din mobilapp

I den här delen ska vi lägga till koden för att registrera tilläggen Användarprofil, Identitet, Livscykel och Signal. Dessa tillägg ingår i [[!UICONTROL Mobile Core Extensions]](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core). Vi måste också registrera Adobe Campaign Standard-tillägget enligt koden nedan.

Öppna projektet i [!DNL Android] studion. Ta bort hela koden i MainApp **förutom den första raden som är din paketprogramsats**.

Klistra in följande kod i MainApp

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

Rad 32 måste du ange[!UICONTROL  Launch] egenskapens miljöfil-ID. Du kommer åt detta från [!UICONTROL environment tab] egenskapens [!UICONTROL Launch] namn.

![launch-id](assets/launch-id-property.PNG)
