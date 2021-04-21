---
title: Steg 1 - Skapa Android-app och konfigurera för att använda Firebase Cloud Messaging
description: I den här delen skapar vi [!DNL Android] App to receive [!UICONTROL Push notifications] skickade från Adobe Campaign Standard. Appen måste vara registrerad med Googles [!DNL Firebase Cloud Service] för att kunna ta emot push-meddelanden.
feature: Tryck
kt: 4825
doc-type: tutorial
activity: use
team: TM
exl-id: f087d9f2-cce9-4903-977f-3c5b47522c06
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 3%

---

# Steg 1 - Skapa [!DNL Android]-appen och konfigurera för att använda [!DNL Firebase Cloud Messaging]

I den här delen skapar du [!DNL Android]-appen som tar emot [!UICONTROL Push notifications] som skickas från Adobe Campaign Standard. Appen måste vara registrerad med Googles [!DNL Firebase Cloud Service] för att kunna ta emot push-meddelanden.

1. Logga in på ditt [!DNL Firebase]-konto.

   [!DNL Firebase] är Googles mobilplattform som hjälper er att snabbt utveckla högkvalitativa appar. Om du inte har något [!DNL Firebase]-konto skapar du ett [härifrån](https://firebase.google.com).

2. Starta [!DNL Android Studio]
3. Klicka på **[!UICONTROL File]** > **[!UICONTROL New]** > **[!UICONTROL New Project].**
4. Markera **[!UICONTROL Empty Activity]** och klicka på **[!UICONTROL Next].**

   ![android-project](assets/android-project.PNG)

5. Ange ett beskrivande namn för projektet.

   I den här demon har vi angett vårt projekt som *[!DNL ACSPushTutorial]*

   ![android-project-configuration](assets/android-project-configuration.PNG)

6. Acceptera standardpaketnamnen och klicka på **[!DNL Finish]** för att skapa projektet.
7. Projektstrukturen bör se ut ungefär som skärmbilden nedan

   ![android-project-structure](assets/android-project-structure.PNG)

8. Klicka på **[!UICONTROL Tools]** > **[!UICONTROL Firebase].** (det lägger till projektet i  [!DNL Firebase])
9. Klicka på **[!UICONTROL Set up Firebase Cloud Messaging].**

   ![setup firebase](assets/android-project-firebase-messaging.PNG)

10. Klicka på **[!UICONTROL Connect to Firebase].**
11. När appen är ansluten till Firebase klickar du på **[!UICONTROL Add FCM to your app].**
12. Klicka på **[!UICONTROL Accept Changes].**

   När du lägger till FCM i programmet måste du ge guiden tillåtelse att göra några ändringar i projektet.

   ![[!DNL add-fcm-to-your-app]](assets/firebase-add-fcm-to-app.PNG)

När appen har integrerats med Firebase bör du få ett meddelande som det som visas nedan:

![[!DNL fcm-successfull]](assets/android-firebase-success.PNG)

[Se till att ditt projekt visas i  [!DNL Firebase ]konsolen](https://console.firebase.google.com/)

## Konfigurera [!UICONTROL Push Channel]-inställningar

1. Logga in på [!DNL Firebase]-konsolen
2. Öppna **[!UICONTROL ACSPushTutorial]**-projektet.
3. Klicka på **kugghjulsikonen** och öppna projektinställningarna

   ![projektinställningar](assets/firebase-project-settings.PNG)

4. Fliken till fliken **[!UICONTROL Cloud Messaging]**.
5. Kopiera servernyckeln

   ![servernyckel](assets/firebase-server-key.PNG)

6. Logga in på din Adobe Campaign Standard-instans
7. Klicka på **[!UICONTROL Adobe Campaign]** > **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL Mobile App].**
8. Välj lämplig **[!UICONTROL Mobile Application Property].**
9. Klicka på ikonen **[!DNL Android]** i **[!UICONTROL Push Channel settings]**-avsnittet.
10. Klistra in servernyckeln i fältet för servernyckeln.

Om allt är bra ska du se ett SUCCESS-meddelande.

![push-channel-settings](assets/push-channel-settings.PNG)

Sammanfattningsvis har vi skapat en [!DNL Android App] och kopplat [!DNL Android App] till [!DNL Firebase]. Vi anslöt sedan mobilappen i Adobe Campaign med [!DNL Android App] genom att klistra in servernyckeln för [!DNL Android]-appen i mobilappen i Adobe Campaign Standard.
