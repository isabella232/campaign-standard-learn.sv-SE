---
title: STEG 4 - Ange identifierare
description: '**pushIdentifier** är en sträng som innehåller enhetstoken för push-meddelanden. Detta är samma token som skickas av Firebase och skickas till SDK med metoden MobileCore.setPushIdentifier.'
feature: Push
topics: MOBILE
kt: 4828
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: a2f194821a9ce06272eaed979ee2d8c62cccac2b
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# Steg 4 - Ställ in [!DNL pushidentifier]

Detta **[!DNL pushidentifier]** är en sträng som innehåller enhetstoken för [!DNL Push] meddelanden. Detta är samma token som skickas av [!DNL Firebase] och skickas till SDK med [!DNL MobileCore.setPushIdentifier] metoden .

Öppna projektet i [!DNL Android ]studion. Ta bort hela koden i [!DNL MainActivity] förutom den första raden som är din paketprogramsats ****.

Klistra in följande kod i [!DNL MainActivity]:

```java{.line-numbers}
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
* Emulatorn bör börja [!DNL Android] och du bör se hur appen körs med [!DNL "Hello World" ]text.
* Öppna [!DNL logcat] fönstret. Sök efter &quot;[!DNL Got]&quot;. Du bör se den token som togs emot från [!DNL Firebase] skrivningen till loggen enligt nedan. Den långa strängen efter &quot;[!DNL Got token]&quot; är [!DNL pushidentifier ]den som skickas till Adobe Campaign.

![logcat-token](assets/logcat-got-token.PNG)

### Kontrollera prenumeranter på mobilprogram

Logga in på din Adobe Campaign Standard-instans.
Navigera **[!UICONTROL Administration->Channels->Mobile App(AEP SDK)]**. Öppna rätt mobilapplikation. Tab to the [!UICONTROL Mobile Application Subscribers] tab. Du borde se en [!UICONTROL registration token ]lista.

![mobile-application-subscribers](assets/mobile-application-subscribers.PNG)

>[OBS!]
>
>Om du inte ser någon registreringstoken på [!UICONTROL Mobile Application Subscribers] fliken STOP här innan du fortsätter.
