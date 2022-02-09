---
title: Steg 1 - Skapa Android-app och konfigurera för att använda Firebase Cloud Messaging
description: I den här delen ska vi skapa [!DNL Android] App som ska tas emot [!UICONTROL Push notifications] skickas från Adobe Campaign Standard. Appen måste vara registrerad hos Google för att du ska kunna ta emot push-meddelanden [!DNL Firebase Cloud Service].
feature: Push
kt: 4825
doc-type: tutorial
activity: use
team: TM
recommendations: noDisplay
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 3%

---

# Steg 1 - Skapa [!DNL Android] Program och konfigurering som ska användas [!DNL Firebase Cloud Messaging]

I den här delen skapar du [!DNL Android] App som ska tas emot [!UICONTROL Push notifications] skickas från Adobe Campaign Standard. Appen måste vara registrerad hos Google för att få push-meddelanden [!DNL Firebase Cloud Service].

1. Logga in på [!DNL Firebase] konto.

   [!DNL Firebase] är Google mobilplattform som hjälper er att snabbt utveckla högkvalitativa appar. Om du inte har en [!DNL Firebase] konto, skapa ett [härifrån](https://firebase.google.com).

2. Starta [!DNL Android Studio]
3. Klicka på **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Markera **[!UICONTROL Empty Activity]** och klicka på **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Ange ett beskrivande namn för projektet.

   I denna demo har vi utsett vårt projekt till *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Acceptera standardpaketnamnen och klicka på **[!DNL Finish]** för att skapa projektet.
7. Projektstrukturen bör se ut ungefär som skärmbilden nedan

   ![android-project-structure](assets/android-project-structure.PNG)

8. Klicka på **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (detta lägger till projektet i [!DNL Firebase])
9. Klicka på **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![setup firebase](assets/android-project-firebase-messaging.PNG)

10. Klicka på **[!UICONTROL Connect to Firebase].**
11. När appen är ansluten till Firebase klickar du på **[!UICONTROL Add FCM to your app].**
12. Klicka på **[!UICONTROL Accept Changes].**

   När du lägger till FCM i programmet måste du ge guiden tillåtelse att göra några ändringar i projektet.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

När appen har integrerats med Firebase bör du få ett meddelande som det som visas nedan:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Se till att ditt projekt finns med i listan [!DNL Firebase ]konsol](https://console.firebase.google.com/)

## Konfigurera [!UICONTROL Push Channel] Inställningar

1. Logga in på [!DNL Firebase] konsol
2. Öppna **[!UICONTROL ACSPushTutorial]** projekt.
3. Klicka på **kugghjulsikon** och öppna projektinställningarna

   ![projektinställningar](assets/firebase-project-settings.PNG)

4. Fliken till **[!UICONTROL Cloud Messaging]** -fliken.
5. Kopiera servernyckeln

   ![servernyckel](assets/firebase-server-key.PNG)

6. Logga in på din Adobe Campaign Standard-instans
7. Klicka på **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Välj lämplig **[!UICONTROL Mobile Application Property].**
9. Klicka på **[!DNL Android]icon** i **[!UICONTROL Push Channel settings]** -avsnitt.
10. Klistra in servernyckeln i fältet för servernyckeln.

Om allt är bra ska du se ett SUCCESS-meddelande.

![push-channel-settings](assets/push-channel-settings.PNG)

Sammanfattningsvis har vi skapat en [!DNL Android App] och kopplade upp [!DNL Android App] med [!DNL Firebase]. Sedan kopplade vi samman mobilappen i Adobe Campaign med [!DNL Android App] genom att klistra in [!DNL Android] Appens servernyckel i mobilappen i Adobe Campaign Standard.
