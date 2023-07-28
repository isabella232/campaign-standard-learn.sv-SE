---
title: STEG 4 - Ange identifierare
description: '**pushIdentifier** är en sträng som innehåller enhetstoken för push-meddelanden. Det är samma token som skickas av Firebase och skickas till SDK med metoden MobileCore.setPushIdentifier.'
feature: Push
user: Admin
level: Experienced
jira: KT-4828
doc-type: tutorial
activity: use
team: TM
exl-id: 08387b84-edaa-45ee-ae66-53bcbd5c7c39
source-git-commit: 757afce50981b96b7820c987308d639a73746c0c
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Steg 4 - Ställ in [!DNL pushidentifier]

The **[!DNL pushidentifier]** är en sträng som innehåller enhetstoken för [!DNL Push] meddelanden. Det är samma token som skickas av [!DNL Firebase] och skickas till SDK med [!DNL MobileCore.setPushIdentifier] -metod.

Öppna projektet i [!DNL Android™]studio. Ta bort hela koden i [!DNL MainActivity] **förutom den första raden som är programsatsen package**.

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
* The [!DNL Android™] emulatorn ska börja och du bör se hur appen körs med [!DNL "Hello World"]text.
* Öppna [!DNL logcat] -fönstret. Sök efter &quot;[!DNL Got]&quot;. Du bör se den token som har tagits emot från [!DNL Firebase] skrivna i loggen enligt nedan. Den långa strängen efter &quot;[!DNL Got token]&quot; är [!DNL pushidentifier]som skickas till Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Kontrollera prenumeranter på mobilprogram

Logga in på din Adobe Campaign Standard-instans.
Navigera **[!UICONTROL Administration->Channels->Mobile App(Experience Platform SDK)]**. Öppna rätt mobilapplikation. Fliken till [!UICONTROL Mobile Application Subscribers] -fliken. Du borde se en [!UICONTROL registration token]listas.

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[!NOTE]
>
>Om du inte ser någon registreringstoken i [!UICONTROL Mobile Application Subscribers] STOPPA här innan du fortsätter.
