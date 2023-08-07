---
title: Förfrågningar om användarens information med Adobe Campaign Standard (ACS) – översikt
description: Självstudiekursen beskriver hur du skapar förfrågningar om användarens information via Adobe Campaign Standard.
feature: Privacy Tools
jira: KT-1480
doc-type: feature video
activity: use
role: Admin
level: Experienced
team: TM
recommendations: noDisplay
exl-id: fb766403-694c-4a7b-b3d1-4a418df85891
source-git-commit: d46e4c84a7d162085016722005cca4aadb4feb3c
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 100%

---

# Förfrågningar om användarens information med användargränssnitt i Adobe Campaign Standard

Adobe Campaign erbjuder personuppgiftsansvariga tre metoder för att utföra förfrågningar om tillgång till användarens information och att radera PII-data i enlighet med sekretessbestämmelser som GDPR (General Data Protection Regulation) och CCPA (California Consumer Privacy Act):

* **Via integration av Privacy Core Service:** Förfrågningar om användarens information som skickas från [!UICONTROL Privacy Service] till alla Experience Cloud-lösningar hanteras automatiskt av Campaign via ett dedikerat arbetsflöde. Mer information om hur du skapar förfrågningar om användarens information från Privacy Core Service finns i [Adobe Experience Platform Privacy Service](https://developer.adobe.com/apis/experienceplatform/gdpr.html).

* **Via API:** Adobe Campaign tillhandahåller ett API för automatisk bearbetning av förfrågningar om användarens information med REST

* **Via Adobe Campaign-gränssnittet:** för varje förfrågan om användarens information skapar den personuppgiftsansvariga en ny förfrågan i Adobe Campaign

>[!NOTE]
>
> **ÄNDRINGAR I ACS 19.4:**
> 
> [Integreringen av Privacy Service](https://developer.adobe.com/apis/experienceplatform/gdpr.html) är den metod du bör använda för alla förfrågningar om åtkomst och radering. Från och med version 19.4 är användningen av API:et och gränssnittet i Campaign för förfrågningar om åtkomst och radering inaktuell. Mer information om inaktuella och borttagna funktioner för Campaign Standard finns på [den här sidan](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=sv).
>
>**Avanmälan för försäljning av personuppgifter (CCPA)**
>
> Som standard finns det ett CCPA-avanmälningsfält i gränssnittet för Campaign och i API:et.
>
> Du kan kontrollera vilken version du har genom att klicka på **?**-ikonen i det övre högra hörnet av gränssnittet och välja Om.

## Självstudiekurser via video

### Krav på förfrågningar om användarens information

1. [Skapa en namnrymd](/help/privacy/namespaces-for-privacy-requests.md)
1. [Ändra anpassade resurser](/help/privacy/custom-resources-for-privacy-requests.md)

### Skapa, spåra och köra förfrågningar om användarens information via användargränssnittet i Adobe Campaign

* [Skapa och spåra förfrågningar om användarens information via användargränssnittet i Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Köra förfrågningar om användarens information](/help/privacy/execute-privacy-requests.md)

## Ytterligare resurser

* [Allmänna riktlinjer för integritetsskydd i Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-management.html?lang=sv#getting-started)
* [CCPA för ACS](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=sv#privacy-requests)
* [Adobe Experience Platform Privacy Service](https://developer.adobe.com/apis/experienceplatform/gdpr.html)
* [Dokumentation för REST API i Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
