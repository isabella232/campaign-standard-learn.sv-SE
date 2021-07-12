---
title: Introduktion till meddelanden i appen
description: Lär dig hur du kan ge användaren sammanhangsberoende meddelanden i appen som svar på en kunds realtidsbeteende i mobilappen.
feature: I appen
kt: 1911
doc-type: feature video
activity: use
team: TM
exl-id: c51716eb-7239-4fc0-9ccf-9f5f0a5fae65
role: User
level: Beginner
source-git-commit: 2be2719ddd84490b796d9abc6300376fa896ff0c
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 21%

---

# Introduktion till [!UICONTROL In-App]-meddelanden {#introduction}

Med kanalen [!UICONTROL In-App Messaging] kan du visa ett meddelande när användaren är aktiv i mobilprogrammet. Den här kanalen kräver att mobilprogram integreras med [!UICONTROL Adobe Experience Platform SDK].

I den här självstudiekursen beskrivs de steg som krävs för att ställa in mobila egenskaper, [!UICONTROL Launch]-tillägget för [!UICONTROL In-App Messaging]-kanalen samt hur du förbereder, anpassar och skickar [!UICONTROL In-App]-meddelanden i Adobe Campaign Standard. Länkarna leder dig till videokurserna om de markerade ämnena.

## Förhandskrav {#prerequisites}

1. Kontrollera att du har åtkomst till **[!UICONTROL In-App]**-kanalen. Om du inte har tillgång till de här kanalerna kontaktar du kontoteamet.
1. Kontrollera att din **användare** har de nödvändiga **behörigheterna** i Adobe Campaign Standard och [!UICONTROL Launch].

   1. Kontrollera att IMS-användaren är en del av grupperna [!UICONTROL Standard User] och [!UICONTROL Administrator] i Adobe Campaign Standard.\
      I det här steget kan användaren logga in på Adobe Campaign Standard, navigera till Experience Platform SDK-mobilappssidan och visa mobilappsegenskaperna som du skapade i [!UICONTROL Launch].
   1. I [!UICONTROL Launch] kontrollerar du att IMS-användaren är en del av en [!UICONTROL Launch]-produktprofil.\
      I det här steget kan användaren logga in på [!UICONTROL Launch] för att skapa och visa egenskaperna. Mer information om produktprofiler i [!UICONTROL Launch] finns i [Skapa din produktprofil](https://docs.adobelaunch.com/launch-reference/administration/user-permissions#3-create-your-product-profile). I produktprofilen bör det inte finnas någon behörighet för företaget eller egenskaperna, men användaren bör fortfarande kunna logga in.

1. I Adobe Experience Platform Launch:

   1. Skapa mobilappen genom att skapa en mobil egenskap och instrumentera mobilappen med Experience Platform SDK.
   1. Installera tillägget **Adobe Campaign Standard** för ditt mobilprogram.

Mer information om tillägg finns i [Konfigurera Campaign Standard-tillägget i Adobe Launch](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-campaign-standard) i [!UICONTROL Adobe Launch ]dokumentationen.

## Steg för att konfigurera [!UICONTROL In-App]-meddelanden {#steps-to-set-up}

1. [Konfigurera en mobil applikation med SDK i Adobe Experience Platform](/help/communication-channels/mobile/configure-mobile-apps-using-aep-sdk.md).

1. [Konfigurera händelser](/help/communication-channels/mobile/in-app/configure-events.md).

## Skapa, hantera och publicera [!UICONTROL In-App]-leveranser {#create-manage-publish}

Du kan antingen skapa engångsleveranser i appen genom att klicka på **[!UICONTROL Create an In-App Message]**-kortet från startsidan, från [!UICONTROL Marketing Activities] eller [Skapa en leverans i appen i ett arbetsflöde](/help/communication-channels/mobile/in-app/in-app-activity.md).

När du ställer in leveransen har du tre alternativ för att rikta in dig till användarna genom att välja bland olika leveransmallar:

1. [**Sänd ett**](/help/communication-channels/mobile/in-app/broadcast-in-app-message.md) meddelande i appen för att nå alla användare i en mobilapp.

   Med den här meddelandetypen kan du skicka meddelanden till alla användare (nuvarande eller framtida) av ditt mobilprogram, även om de inte har en befintlig profil i Adobe Campaign. Personalisering är därför inte möjligt när du anpassar meddelanden eftersom användarprofilen inte nödvändigtvis finns i Adobe Campaign.

1. Alla användare målgruppsanpassas utifrån deras mobilappsprofil.

   Den här meddelandetypen gör att du kan rikta indig på alla kända eller anonyma användare av en mobilapp som har en mobilprofil i Adobe Campaign. Den här meddelandetypen kan endast anpassas med icke-personliga och icke-känsliga attribut och kräver ingen säker handskakning mellan Mobile SDK och Adobe Campaigns meddelandetjänst i appen. Därför baseras personaliseringsstrategin på vad ni har lärt er om användarna av deras interaktion med enheten. Till exempel alla användare som har startat sin app mer än fem gånger under den senaste veckan.

1. [**Målinrikta användare baserat på deras profil i Campaign**](/help/communication-channels/mobile/in-app/target-users-based-on-campaign-profile.md).

   Den här meddelandetypen gör att du kan ange Adobe Campaign-profiler (CRM-profiler) som prenumererar på ditt mobilprogram som mål. Meddelandet kan anpassas med alla tillgängliga profilattribut i Adobe Campaign, men kräver en säker handskakning mellan Mobile SDK och Campaigns meddelandetjänst i appen för att säkerställa att meddelanden med personlig och känslig information endast används av behöriga användare.

Den här mallen är användbar för att stödja flerkanalsanvändning, där du redan har riktat in användare på andra kanaler som e-post eller push och baserat på deras svar, vill du engagera dem med ett meddelande i appen.

## Rapportera om leveranser i appen {#report}

När leveransen har publicerats kan du [rapportera leveransen i appen](/help/communication-channels/mobile/in-app/in-app-reporting.md).

## Ytterligare resurser

* [Rapport i appen](https://docs.adobe.com/content/help/en/campaign-standard/using/reporting/list-of-reports/in-app-report.html)
* [Konfigurera en mobil egenskap](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property)
* [Konfigurera ett mobilprogram med Adobe Experience Platform SDK](https://helpx.adobe.com/se/campaign/kb/configuring-app-sdk.html)
* [Förbereda och skicka ett meddelande i appen](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/preparing-and-sending-an-in-app-message.html)
* [Anpassa ett meddelande i appen](https://docs.adobe.com/content/help/en/campaign-standard/using/communication-channels/in-app-messaging/customizing-an-in-app-message.html)
* [Skicka ett meddelande i appen i ett arbetsflöde](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/channel-activities/in-app-delivery.html)
* [Aktivera livscykelvärden](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
