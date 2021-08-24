---
title: Förfrågningar om användarens information med Adobe Campaign Standard (ACS) – översikt
description: I självstudiekursen beskrivs hur du skapar sekretessförfrågningar via Adobe Campaign Standard gränssnitt.
feature: Sekretessverktyg
kt: 1480
doc-type: feature video
activity: use
team: TM
exl-id: fb766403-694c-4a7b-b3d1-4a418df85891
source-git-commit: 481cbdcc9ac7446cc36fbff6e3d6e43fe333d30b
workflow-type: tm+mt
source-wordcount: '351'
ht-degree: 62%

---

# Förfrågningar om användarens information med användargränssnitt i Adobe Campaign Standard

Adobe Campaign erbjuder personuppgiftsansvariga tre metoder för att utföra förfrågningar om tillgång till användarens information och att radera PII-data i enlighet med sekretessbestämmelser som GDPR (General Data Protection Regulation) och CCPA (California Consumer Privacy Act):

* **Via integration av Privacy Core Service:** Förfrågningar om användarens information som skickas från [!UICONTROL Privacy Service] till alla Experience Cloud-lösningar hanteras automatiskt av Campaign via ett dedikerat arbetsflöde. Mer information om hur du skapar sekretessförfrågningar från tjänsten Integritet finns i [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)

* **Via API:** Adobe Campaign tillhandahåller ett API som tillåter automatisk behandling av förfrågningar om användarens information med REST

* **Via Adobe Campaign-gränssnittet:** för varje sekretessförfrågan skapar den personuppgiftsansvariga en sekretessförfrågan i Adobe Campaign

>[!NOTE]
>
> **ÄNDRINGAR I ACS 19.4:**
> 
> Integreringen av [Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html) är den metod du bör använda för alla förfrågningar om åtkomst och radering. Från och med version 19.4 är användningen av API:et och gränssnittet i Campaign för förfrågningar om åtkomst och radering inaktuell. Mer information om inaktuella och borttagna funktioner för Campaign Standard finns på [den här sidan](https://experienceleague.adobe.com/docs/campaign-standard/using/release-notes/deprecated-features.html?lang=en).
>
>**Avanmäl dig till försäljning av personuppgifter (CCPA)**
>
> Ett CCPA-fält för avanmälan finns i körklart läge i Campaign-gränssnittet och API:t.
>
> Du kan kontrollera vilken version du har genom att klicka på **?** i det övre högra hörnet av gränssnittet och välja Om.

## Självstudiekurser via video

### Krav på förfrågningar om användarens information

1. [Skapa en namnrymd](/help/privacy/namespaces-for-privacy-requests.md)
1. [Ändra anpassade resurser](/help/privacy/custom-resources-for-privacy-requests.md)

### Skapa, spåra och köra sekretessförfrågningar via Adobe Campaign användargränssnitt

* [Skapa och spåra förfrågningar om användarens information via användargränssnittet för Adobe Campaign](/help/privacy/create-and-track-privacy-requests.md)
* [Köra förfrågningar om användarens information](/help/privacy/execute-privacy-requests.md)

## Ytterligare resurser

* [Allmänna riktlinjer för integritetsskydd i Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/getting-started/privacy/privacy-management.html?lang=en#getting-started)
* [CCPA för ACS](https://experienceleague.adobe.com/docs/campaign-standard/using/getting-started/privacy/privacy-requests.html?lang=en#privacy-requests)
* [Adobe Experience Platform Privacy Service](https://www.adobe.io/apis/experienceplatform/gdpr.html)
* [Dokumentation för REST API i Adobe Campaign Standard](https://final-docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#privacy-management)
