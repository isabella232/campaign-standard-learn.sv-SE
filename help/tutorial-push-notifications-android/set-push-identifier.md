---
title: STEG 4 - Ange identifierare
description: '**pushIdentifier** är en sträng som innehåller enhetstoken för push-meddelanden. Detta är samma token som skickas av Firebase och skickas till SDK med metoden MobileCore.setPushIdentifier.'
feature: Tryck
topic: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
translation-type: tm+mt
source-git-commit: ddbb0843ea45a83d9ab5bfa0877287f6ba7d6210
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---

# Steg 4 - Ange [!DNL pushidentifier]

**[!DNL pushidentifier]** är en sträng som innehåller enhetstoken för [!DNL Push]-meddelanden. Detta är samma token som skickas av [!DNL Firebase] och skickas till SDK med metoden [!DNL MobileCore.setPushIdentifier].

Öppna projektet i [!DNL Android ]studio. Ta bort hela koden i [!DNL MainActivity] **förutom den första raden som är din paketsats**.

Klistra in följande kod i [!DNL MainActivity]:

<!--
Removed `{.line-numbers}` below
-->

```java
import androidx.annotation.NonNull;
import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.util.Log;
import android.widget.Toast;

import com.adobe.marketing.mobile.MobileCore;
import com.google.android.gms.tasks.OnCompleteListener;
import com.google.android.gms.tasks.Task;
import com.google.firebase.iid.FirebaseInstanceId;
import com.google.firebase.iid.InstanceIdResult;

public class MainActivity extends AppCompatActivity {

@Override
protected void onCreate(Bundle savedInstanceState) {
super.onCreate(savedInstanceState);
setContentView(R.layout.activity_main);

registerToken();
}

void registerToken() {
FirebaseInstanceId.getInstance().getInstanceId()
    .addOnCompleteListener(new OnCompleteListener<InstanceIdResult>() {
        @Override
        public void onComplete(@NonNull Task<InstanceIdResult> task) {
            if (!task.isSuccessful()) {
                Log.w("Message App", "getInstanceId failed", task.getException());
                return;
            }

// Get new Instance ID token
String token = task.getResult().getToken();

Log.d("Got token", token);

MobileCore.setPushIdentifier(token);
}
});
}

@Override
public void onResume() {
super.onResume();
MobileCore.setApplication(getApplication());
MobileCore.lifecycleStart(null);
}

@Override
public void onPause() {
super.onPause();
MobileCore.lifecyclePause();
}
}
```

## Testa din app

Nu är det ett bra tillfälle att testa appen innan du går vidare.

* Kör appen genom att klicka på den gröna pilen eller välj **[!DNL Run->Run'app']**.
* Emulatorn [!DNL Android] ska starta och du bör se programmet köras med [!DNL "Hello World" ]text.
* Öppna fönstret [!DNL logcat]. Sök efter [!DNL Got]. Du bör se den token som togs emot från [!DNL Firebase] skriven i loggen enligt nedan. Den långa strängen efter &quot;[!DNL Got token]&quot; är den [!DNL pushidentifier ]som skickas till Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Kontrollera prenumeranter på mobilprogram

Logga in på din Adobe Campaign Standard-instans.
Navigera till **[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**. Öppna rätt mobilapplikation. Fliken till fliken [!UICONTROL Mobile Application Subscribers]. Du bör se en [!UICONTROL registration token ]lista.

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Om du inte ser någon registreringstoken på fliken [!UICONTROL Mobile Application Subscribers] STOPPAR du här innan du fortsätter.
