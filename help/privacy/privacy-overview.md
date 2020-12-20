---
title: Sekretessförfrågningar med Adobe Campaign Standard (ACS) - översikt
description: I självstudiekursen beskrivs hur du skapar sekretessförfrågningar via Adobe Campaign Standard-gränssnittet (ACS).
feature: GDPR, CCAP
topic: Privacy
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 20%

---


# Sekretessförfrågningar med Adobe Campaign Standard användargränssnitt

Adobe Campaign erbjuder personuppgiftsansvariga tre metoder för att utföra förfrågningar om sekretessåtkomst och radering av PII-data i enlighet med sekretessbestämmelser som GDPR (General Data Protection Regulation) och CCPA (California Consumer Privacy Act):

* **Via integreringen av bastjänsten för skydd av privatlivet:** sekretessförfrågningar som skickas  [!UICONTROL Privacy Service] till alla Experience Cloud-lösningar hanteras automatiskt av Campaign via ett dedikerat arbetsflöde. Läs mer i [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) om du vill veta hur du skapar sekretessförfrågningar från bastjänsten för sekretess

* **Via API:** Adobe Campaign tillhandahåller ett API som tillåter automatisk behandling av sekretessförfrågningar med REST

* **Via Adobe Campaign-gränssnittet:** för varje sekretessförfrågan skapar den personuppgiftsansvariga en ny sekretessförfrågan i Adobe Campaign

>[!NOTE]
>
> **ÄNDRINGAR I ACS 19.4:**
> 
> [Integrering av Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) är den metod du bör använda för alla begäranden om åtkomst och borttagning. Från och med 19.4 är användningen av Campaign-API:t och gränssnittet för begäran om åtkomst och borttagning föråldrad. Mer information om borttagna och borttagna funktioner för Campaign Standard finns på [den här sidan](https://helpx.adobe.com/se/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Avanmäl dig till försäljning av personuppgifter (CCPA)**
>
>Från och med 19.4 finns det ett CCPA-avanmälningsfält i gränssnittet och i API:et i Campaign. För att 19.3 ska kunna utnyttja denna information måste du skapa det här fältet i Adobe Campaign Standard. Mer information finns i [den detaljerade dokumentationen](https://helpx.adobe.com/se/campaign/kb/acs-privacy.html#ccpa).
>
> Du kan se vilken version du har genom att klicka på ? i det övre högra hörnet av gränssnittet och välja Om.

## Video Tutorials

### Krav för sekretessförfrågningar

1. [Skapa ett namnutrymme](/help/privacy/namespaces-for-privacy-requests.md)
1. [Ändra anpassade resurser](/help/privacy/custom-resources-for-privacy-requests.md)

### Skapa, spåra och köra sekretessförfrågningar via Adobe Campaign användargränssnitt

* [Skapa och spåra sekretessförfrågningar via Adobe Campaign användargränssnitt](/help/privacy/create-and-track-privacy-requests.md)
* [Kör sekretessbegäranden](/help/privacy/execute-privacy-requests.md)

## Ytterligare resurser

* [Allmänna riktlinjer för integritetsskydd i Campaign](https://helpx.adobe.com/se/campaign/kb/campaign-privacy-overview.html)
* [CCPA för ACS](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Adobe Campaign Standard REST API-dokumentation](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
