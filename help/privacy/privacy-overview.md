---
title: Sekretessförfrågningar med Adobe Campaign Standard (ACS) - översikt
description: I självstudiekursen beskrivs hur du skapar sekretessförfrågningar via gränssnittet för Adobe Campaign Standard (ACS).
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
ht-degree: 0%

---


# Sekretessförfrågningar med Adobe Campaign Standard User Interface

Adobe Campaign erbjuder personuppgiftsansvariga tre metoder för att utföra sekretessåtkomst och ta bort förfrågningar om PII-data i enlighet med sekretessbestämmelser som GDPR (General Data Protection Regulation) och CCPA (California Consumer Privacy Act):

* **Via integreringen av integritetspolicyn Core Service:** Sekretessförfrågningar som skickas från [!UICONTROL Privacy Service] till alla Experience Cloud-lösningar hanteras automatiskt av Campaign via ett dedikerat arbetsflöde. Läs mer i [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) om hur du skapar sekretessförfrågningar från Privacy Core-tjänsten

* **Via API:** Adobe Campaign tillhandahåller ett API som möjliggör automatisk behandling av sekretessförfrågningar med REST

* **Via gränssnittet i Adobe Campaign:** för varje sekretessförfrågan skapar den personuppgiftsansvarige en ny sekretessförfrågan i Adobe Campaign

>[!NOTE]
>
> **ÄNDRINGAR I ACS 19.4:**
> 
> Integreringen [av](https://adobe.io/apis/cloudplatform/gdpr.html) Integritetstjänsten är den metod du bör använda för alla begäranden om åtkomst och borttagning. Från och med 19.4 är användningen av Campaign-API:t och gränssnittet för begäran om åtkomst och borttagning föråldrad. Mer information om borttagna och borttagna funktioner i Campaign Standard finns på [den här sidan](https://helpx.adobe.com/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Avanmäl dig till försäljning av personuppgifter (CCPA)**
>
>Från och med 19.4 finns det ett CCPA-avanmälningsfält som är klart i Campaign-gränssnittet och API:t. För att 19.3 ska kunna utnyttja denna information måste du skapa det här fältet i Adobe Campaign Standard. Mer information finns i den [detaljerade dokumentationen](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa) .
>
> Du kan kontrollera versionen genom att klicka på ? i det övre högra hörnet av gränssnittet och väljer Om.

## Videokurser

### Krav för sekretessförfrågningar

1. [Skapa ett namnutrymme](/help/privacy/namespaces-for-privacy-requests.md)
1. [Ändra anpassade resurser](/help/privacy/custom-resources-for-privacy-requests.md)

### Skapa, spåra och köra sekretessförfrågningar via användargränssnittet i Adobe Campaign

* [Skapa och spåra sekretessförfrågningar via användargränssnittet i Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Kör sekretessbegäranden](/help/privacy/execute-privacy-requests.md)

## Ytterligare resurser

* [Allmänna riktlinjer för integritetsskydd för Campaign](https://helpx.adobe.com/campaign/kb/campaign-privacy-overview.html)
* [CCPA för ACS](https://helpx.adobe.com/campaign/kb/acs-privacy.html#ccpa)
* [Integritetstjänst för Adobe Experience Platform](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Adobe Campaign Standard REST API-dokumentation](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
