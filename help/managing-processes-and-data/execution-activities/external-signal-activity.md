---
title: Extern signalaktivitet - Anropa ett arbetsflöde med parametrar
description: Den externa signalaktiviteten används för att organisera och samordna olika processer som ingår i samma kundresa till olika arbetsflöden. Det gör att man kan starta ett arbetsflöde från ett annat, vilket ger stöd för mer komplexa kundresor samtidigt som man bättre kan övervaka och reagera i händelse av problem.
feature: External Signal Activity
topics: Workflows
kt: 2750
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: b95fb2360d6336c941e7b92a6e2abb376185a7c3
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 0%

---


# [!UICONTROL External Signal activity ]- Anropa ett arbetsflöde med parametrar

Det [!UICONTROL External Signal activity] används för att organisera och samordna olika processer som ingår i samma kundresa till olika arbetsflöden. Det gör att man kan starta ett arbetsflöde från ett annat, vilket ger stöd för mer komplexa kundresor samtidigt som man bättre kan övervaka och reagera i händelse av problem.

I ACS 19.2 [!UICONTROL External Signal activity] kan användaren inte bara anropa ett arbetsflöde utan även skicka parametrar till arbetsflödet (ett målgruppsnamn, ett filnamn som ska importeras, en del av meddelandeinnehållet osv.) till arbetsflödet från ett annat arbetsflöde eller ett REST API-anrop för integrering med dina externa system.

Detta inkluderar även en ny **testaktivitet** där du kan köra tester på den här funktionen.

I följande video förklaras de konfigurationssteg som krävs för att:

1. **Ta emot externa parametrar** från ett externt system, som ett innehållshanteringssystem (CRM):

   * Deklarera parametrarna i den externa signalaktiviteten
   * Konfigurera API-anropet för att definiera parametrarna och utlösa arbetsflödet för extern signalaktivitet. Mer information om hur du konfigurerar ett API-anrop finns i [Utlösa en signalaktivitet](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity).

1. **Anpassa ett arbetsflöde med externa parametrar** (händelsevariabler):

   När arbetsflödet har utlösts hämtas parametrarna in i arbetsflödets händelsevariabler och kan användas i arbetsflödet. Se [dokumentationen](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) för alla aktiviteter som kan anpassas med händelsevariabler:

   * Konfigurera testaktiviteten (nytt i 19.2)
   * Konfigurera aktiviteten Läs målgrupp och E-postleverans

1. **Konfigurera en slutaktivitet** för att anropa ett arbetsflöde med externa parametrar

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Ytterligare resurser

* [Extern signal (dokumentation)](https://docs.adobe.com/content/help/en/campaign-standard/using/managing-processes-and-data/data-management-activities/external-api.html)
