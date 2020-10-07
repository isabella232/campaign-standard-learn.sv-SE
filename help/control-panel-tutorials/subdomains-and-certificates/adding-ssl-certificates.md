---
title: Lägga till SSL-certifikat
description: Med kontrollpanelen i Adobe Campaign kan du lägga till SSL-certifikat för att skydda underdomänerna.
feature: Control Panel
topics: null
audience: administrator
kt: 4219
thumbnail: 31317.jpg
doc-type: feature video
activity: use
team: PM
translation-type: tm+mt
source-git-commit: 05550c50713e65793309e51355a8e31683f81e0b
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 54%

---


# Lägga till SSL-certifikat

Med [!UICONTROL Adobe Campaign Control Panel] i kan du lägga till SSL-certifikat för att skydda underdomänerna.

## Åtkomst till [!UICONTROL Control Panel] för att hantera underdomäner

För att få åtkomst till hantering av underdomäner i [!UICONTROL Control Panel] ska du gå till:

* [Experience Cloud Home](https://experience.adobe.com/#/home) > [!UICONTROL Solution picker]: [!DNL Campaign] > **[!UICONTROL Control Panel]** card > [!UICONTROL **Subdomains &amp; Certificates**] card

   eller
* Direkt från webbadressen: [https://experience.adobe.com/#/controlpanel/domain](https://experience.adobe.com/#/controlpanel/domain)

## Stegvis lägga till SSL-certifikat

Att lägga till SSL-certifikat kräver tre steg:

### Steg 1: Generera [!UICONTROL Certificate Signing Requests]

The [!UICONTROL Certificate Signing Request] (CSR) is required for the purchase of a SSL certificate. Den måste genereras för instansen och de underdomäner som du planerar att skydda.

I videon nedan beskrivs hur du genererar ett [!UICONTROL Certificate Signing Request] i [!UICONTROL Control Panel].

>[!VIDEO](https://video.tv.adobe.com/v/31317?quality=12)

*Skapa en begäran om certifikatsignering (02:36 min)*

### Steg 2: Köp SSL-certifikat

När CSR har erhållits köper du SSL-certifikatet från en certifikatutfärdare som har godkänts av organisationen.

### Steg 3: Installera SSL-certifikat

När du har fått SSL-certifikatet måste det vara installerat för de underdomäner som du planerar att skydda.

I videon nedan förklaras hur du installerar SSL-certifikat i [!UICONTROL Control Panel].

>[!VIDEO](https://video.tv.adobe.com/v/31166?quality=12)

*Installera SSL-certifikat (01:25 min)*

## Ytterligare resurser

* [Delegera underdomäner](/help/administrating/control-panel/subdomain-delegation.md)
* [Underdomäner och certifikat – dokumentation](https://docs.adobe.com/content/help/sv-SE/control-panel/using/subdomains-and-certificates/renewing-subdomain-certificate.html)
