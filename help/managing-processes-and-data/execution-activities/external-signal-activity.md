---
title: Extern signalaktivitet - Anropa ett arbetsflöde med parametrar
description: Lär dig hur du startar ett arbetsflöde från ett annat för att stödja mer komplexa kundresor, samtidigt som du får bättre möjlighet att övervaka och reagera på problem.
feature: Körningsaktivitet
kt: 2750
thumbnail: 27249
doc-type: feature video
activity: use
team: TM
exl-id: d3996185-681c-4906-85f0-0543ab767519
role: Business Practitioner, Developer
level: Experienced
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 9%

---

# [!UICONTROL External Signal activity ]- Anropa ett arbetsflöde med parametrar

[!UICONTROL External Signal activity] används för att organisera och samordna olika processer som ingår i samma kundresa till olika arbetsflöden. Det gör att man kan starta ett arbetsflöde från ett annat, vilket ger stöd för mer komplexa kundresor samtidigt som man bättre kan övervaka och reagera vid problem.

I ACS 19.2 kan [!UICONTROL External Signal activity] inte bara anropa ett arbetsflöde, utan dessutom skicka parametrar till arbetsflödet (ett målgruppsnamn, ett filnamn som ska importeras, en del av meddelandeinnehållet osv.) till arbetsflödet från ett annat arbetsflöde eller ett REST API-anrop för integrering med dina externa system.

Detta inkluderar även en ny **Test**-aktivitet där du kan köra tester på den här funktionen.

I följande video förklaras de konfigurationssteg som krävs för att:

1. **Ta emot externa** parametrar från ett externt system, som ett innehållshanteringssystem (CRM):

   * Deklarera parametrarna i den externa signalaktiviteten
   * Konfigurera API-anropet för att definiera parametrarna och utlösa arbetsflödet för extern signalaktivitet. Mer information om hur du konfigurerar ett API-anrop finns i [Utlösa en signalaktivitet](https://docs.campaign.adobe.com/doc/standard/en/api/ACS_API.html#triggering-a-signal-activity).

1. **Anpassa ett arbetsflöde med externa parametrar**  (händelsevariabler):

   När arbetsflödet har utlösts hämtas parametrarna in i arbetsflödets händelsevariabler och kan användas i arbetsflödet. Se [dokumentationen](https://helpx.adobe.com/campaign/standard/automating/using/calling-a-workflow-with-external-parameters.html) för alla aktiviteter som kan anpassas med händelsevariabler:

   * Konfigurera testaktiviteten (nytt i 19.2)
   * Konfigurera aktiviteten Läs målgrupp och E-postleverans

1. **Konfigurera en End** Activity för att anropa ett arbetsflöde med externa parametrar

>[!VIDEO](https://video.tv.adobe.com/v/27249/?quality=12)

## Ytterligare resurser

* [Extern signal (dokumentation)](https://experienceleague.adobe.com/docs/campaign-standard/using/managing-processes-and-data/calling-workflow-external-parameters/calling-a-workflow-with-external-parameters.html)
