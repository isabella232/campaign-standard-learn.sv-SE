---
title: Förfrågningar om användarens information med Adobe Campaign Standard (ACS) – översikt
description: Självstudiekursen beskriver hur du skapar förfrågningar om användarens information via Adobe Campaign Standard-gränssnittet (ACS).
feature: GDPR, CCAP
topic: Sekretess
kt: 1480
doc-type: feature video
activity: use
team: TM
translation-type: ht
source-git-commit: 556bff4c94e16d3a94561dee1ccb311bc003b631
workflow-type: ht
source-wordcount: '371'
ht-degree: 100%

---


# Förfrågningar om användarens information med användargränssnitt i Adobe Campaign Standard

Adobe Campaign erbjuder personuppgiftsansvariga tre metoder för att utföra förfrågningar om tillgång till användarens information och att radera PII-data i enlighet med sekretessbestämmelser som GDPR (General Data Protection Regulation) och CCPA (California Consumer Privacy Act):

* **Via integration av Privacy Core Service:** Förfrågningar om användarens information som skickas från [!UICONTROL Privacy Service] till alla Experience Cloud-lösningar hanteras automatiskt av Campaign via ett dedikerat arbetsflöde. Läs dokumentationen för [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) om hur du skapar förfrågningar om användarens information via Privacy Core Service

* **Via API:** Adobe Campaign tillhandahåller ett API som tillåter automatisk behandling av förfrågningar om användarens information med REST

* **Via Adobe Campaign-gränssnittet:** för varje förfrågan om användarens information skapar den personuppgiftsansvariga en ny förfrågan i Adobe Campaign

>[!NOTE]
>
> **ÄNDRINGAR I ACS 19.4:**
> 
> Integreringen av [Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html) är den metod du bör använda för alla förfrågningar om åtkomst och radering. Från och med version 19.4 är användningen av API:et och gränssnittet i Campaign för förfrågningar om åtkomst och radering inaktuell. Mer information om inaktuella och borttagna funktioner för Campaign Standard finns på [den här sidan](https://helpx.adobe.com/se/campaign/kb/acs-deprecated-and-removed-features.html).
>
>**Avanmäl dig till försäljning av personuppgifter (CCPA)**
>
>Från och med 19.4 finns det ett CCPA-avanmälningsfält i gränssnittet och i API:et i Campaign. För att kunna dra nytta av denna information i 19.3 måste du skapa detta fält i Adobe Campaign Standard. Mer information finns i den [detaljerade dokumentationen](https://helpx.adobe.com/se/campaign/kb/acs-privacy.html#ccpa).
>
> Du kan se vilken version du har genom att klicka på ? i det övre högra hörnet av gränssnittet och välja Om.

## Självstudiekurser via video

### Krav på förfrågningar om användarens information

1. [Skapa en namnrymd](/help/privacy/namespaces-for-privacy-requests.md)
1. [Ändra anpassade resurser](/help/privacy/custom-resources-for-privacy-requests.md)

### Skapa, spåra och köra förfrågningar om användarens information via användargränssnittet för Adobe Campaign

* [Skapa och spåra förfrågningar om användarens information via användargränssnittet för Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Köra förfrågningar om användarens information](/help/privacy/execute-privacy-requests.md)

## Ytterligare resurser

* [Allmänna riktlinjer för integritetsskydd i Campaign](https://helpx.adobe.com/se/campaign/kb/campaign-privacy-overview.html)
* [CCPA för ACS](https://helpx.adobe.com/se/campaign/kb/acs-privacy.html#ccpa)
* [Adobe Experience Platform Privacy Service](https://adobe.io/apis/cloudplatform/gdpr.html)
* [Dokumentation för REST API i Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
