---
title: Konfigurera händelser
description: 'När du konfigurerar ett meddelande i appen i Adobe Campaign Standard-händelser (ACS) definierar du vilken användarinitierad åtgärd som ska utlösa meddelandet som ska visas. '
feature: In-App
topics: Mobile
kt: 2548
doc-type: feature video
activity: use
team: TM
translation-type: tm+mt
source-git-commit: 82fb2d39dc61a55c0aa20ca1fa215f35a7dd9088
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 2%

---


# Konfigurera [!UICONTROL Events] {#configuring-events}

När du konfigurerar ett [!UICONTROL In-App] meddelande måste du definiera vilken användarinitierad åtgärd som utlöser meddelandet som ska visas. Dessa åtgärder anropas [!UICONTROL events]. Tre kategorier [!UICONTROL events] är tillgängliga: [!UICONTROL Mobile Application events], [!UICONTROL Life Cycle events]och [!UICONTROL Analytics events].

## [!UICONTROL Mobile Application Events] {#mobile-application-events}

[!UICONTROL Mobile Application events] som [!UICONTROL custom events] implementeras i ditt mobilprogram.

Exempel:

* En kund har visat en artikel
* En kund lägger till en artikel i kundvagnen
* Övergivna kundvagnar
* En kund har köpt något

Du måste konfigurera dessa [!UICONTROL events] i Adobe Campaign. I följande video beskrivs hur du gör detta.

>[!VIDEO](https://video.tv.adobe.com/v/26245?quality=12)

## [!UICONTROL Life Cycle events]  {#life-cycle-events}

[!UICONTROL Lifecycle events] är färdiga [!UICONTROL events]. The following [!UICONTROL events] are available:

* [!UICONTROL launched]
* [!UICONTROL upgraded]
* [!UICONTROL crashed]

Ett exempel kan vara ett meddelande som presenterar nya funktioner efter en uppgradering eller en eventkampanj.

>[!NOTE]
>
>De måste [!UICONTROL Lifecycle module] konfigureras i mobilprogrammet. Mer information om [hur du lägger till en livscykel i din app finns här](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/mobile-core/lifecycle)

## [!UICONTROL Analytics Events] {#analytics-events}

Följande tre kategorier stöds beroende på vad som finns i din mobilapp:

* Adobe Analytics
* [!UICONTROL Context data]
* [!UICONTROL View state]

>[!NOTE]
>
>[!UICONTROL Analytics events] kräver en Adobe Analytics-licens. När du har konfigurerat [[!DNL Analytics] ](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#configure-analytics-extension-in-launch) tillägget och lagt till [Analytics i appen](https://aep-sdks.gitbook.io/docs/using-mobile-extensions/adobe-analytics#add-analytics-to-your-app)blir dessa händelser tillgängliga i ACS- [!UICONTROL In-App] konfigurationen.

## Ytterligare resurser

* [Aktivera livscykelvärden (dokumentation)](https://aep-sdks.gitbook.io/docs/getting-started/initialize-the-sdk#enable-lifecycle-metrics)
