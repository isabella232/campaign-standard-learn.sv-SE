---
title: Steg 1 - Skapa Android-app och konfigurera för att använda Firebase Cloud Messaging
description: I den här delen skapar vi [!DNL Android]-appen som tar emot [!UICONTROL Push-meddelanden] som skickas från Adobe Campaign Standard. För att få push-meddelanden måste appen vara registrerad med Googles [!DNL Firebase Cloud Service].
feature: Push
topics: Mobile
kt: 4825
doc-type: tutorial
activity: use
team: TM
translation-type: tm+mt
source-git-commit: afe1ae6c8d73b7b776e0eec327fa16db76c23ce1
workflow-type: tm+mt
source-wordcount: '330'
ht-degree: 1%

---


# Steg 1 - Skapa [!DNL Android] program och konfigurera för att använda [!DNL Firebase Cloud Messaging]

I den här delen skapar du [!DNL Android] en app som ska tas emot [!UICONTROL Push notifications] från Adobe Campaign Standard. För att få push-meddelanden måste appen vara registrerad hos Googles [!DNL Firebase Cloud Service].

1. Logga in på ditt [!DNL Firebase] konto.

   [!DNL Firebase] är Googles mobilplattform som hjälper er att snabbt utveckla högkvalitativa appar. Om du inte har något [!DNL Firebase] konto kan du skapa ett [härifrån](https://firebase.google.com).

2. Starta [!DNL Android Studio]
3. Klicka på **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Markera **[!UICONTROL Empty Activity]** och klicka **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Ange ett beskrivande namn för projektet.

   I denna demo har vi utsett vårt projekt till *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Acceptera standardpaketnamnen och klicka för **[!DNL Finish]** att skapa projektet.
7. Projektstrukturen bör se ut ungefär som skärmbilden nedan

   ![android-project-structure](assets/android-project-structure.PNG)

8. Klicka på **[!UICONTROL Tools]** > **[!UICONTROL Firebase].**(det lägger till projektet i[!DNL Firebase])
9. Klicka på **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![setup firebase](assets/android-project-firebase-messaging.PNG)

10. Klicka på **[!UICONTROL Connect to Firebase].**
11. När appen är ansluten till Firebase klickar du på **[!UICONTROL Add FCM to your app].**
12. Klicka på **[!UICONTROL Accept Changes].**

   När du lägger till FCM i programmet måste du ge guiden tillåtelse att göra några ändringar i projektet.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

När appen har integrerats med Firebase bör du få ett meddelande som det som visas nedan:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Se till att ditt projekt finns med i listan i konsolen [!DNL Firebase ]](https://console.firebase.google.com/)

## Konfigurera [!UICONTROL Push Channel] inställningar

1. Logga in på [!DNL Firebase] konsolen
2. Öppna **[!UICONTROL ACSPushTutorial]** projektet.
3. Klicka på **kugghjulsikonen** och öppna projektinställningarna

   ![projektinställningar](assets/firebase-project-settings.PNG)

4. Tab to the **[!UICONTROL Cloud Messaging]** tab.
5. Kopiera servernyckeln

   ![servernyckel](assets/firebase-server-key.PNG)

6. Logga in på din instans av Adobe Campaign Standard
7. Klicka på **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Välj lämplig **[!UICONTROL Mobile Application Property].**
9. Klicka på **[!DNL Android]ikonen **i **[!UICONTROL Push Channel settings]**avsnittet.
10. Klistra in servernyckeln i fältet för servernyckeln.

Om allt är bra ska du se ett SUCCESS-meddelande.

![push-channel-settings](assets/push-channel-settings.PNG)

Sammanfattningsvis har vi skapat en [!DNL Android App] och kopplat samman [!DNL Android App] den med [!DNL Firebase]. Sedan kopplade vi samman mobilappen i Adobe Campaign med [!DNL Android App] genom att klistra in [!DNL Android] appens servernyckel i mobilappen i Adobe Campaign Standard.
