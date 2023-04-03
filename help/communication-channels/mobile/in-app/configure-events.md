---
title: Konfigurera händelser
description: "Förstå hur händelser definierar vilken användarinitierad åtgärd som utlöser ett meddelande i appen som ska visas. "
feature: In App
kt: 2548
thumbnail: 26245.jpg
doc-type: feature video
activity: use
team: TM
exl-id: 2c7937f4-b0da-46e5-934e-c660012c2c6f
role: User, Developer
level: Beginner, Intermediate
source-git-commit: 89df23d00913d36b93d3be03b62c74320524f9c7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---

# Konfigurera [!UICONTROL Events] {#configuring-events}

När en [!UICONTROL In-App] måste du definiera vilken användarinitierad åtgärd som utlöser meddelandet som ska visas. Dessa åtgärder anropas [!UICONTROL events]. Tre kategorier av [!UICONTROL events] är tillgängliga: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events]och [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] är [!UICONTROL custom events] som implementeras i ditt mobilprogram.

Exempel:

* En kund har visat en artikel
* En kund lägger till en artikel i kundvagnen
* Övergivna kundvagnar
* En kund har köpt något

Du måste konfigurera dessa [!UICONTROL events] i Adobe Campaign. I följande video beskrivs hur du gör detta.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12&learn=on)

## [!UICONTROL Life Cycle events] {#life-cycle-events}

[!UICONTROL Lifecycle events] är körklara [!UICONTROL events]. Följande [!UICONTROL events] är tillgängliga:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Ett exempel kan vara ett meddelande som presenterar nya funktioner efter en uppgradering eller en eventkampanj.

>[!NOTE]
>
>The [!UICONTROL Lifecycle module] måste konfigureras i mobilprogrammet. Mer information om [Lägga till livscykeln i appen](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

Följande tre kategorier stöds beroende på vad som finns i din mobilapp:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] kräver en Adobe Analytics-licens. När du har [[!DNL Analytics] tillägg konfigurerat](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) och har lagts till [Analyser för er app](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app), blir dessa händelser tillgängliga i [!UICONTROL In-App] konfiguration i ACS.
