---
title: Microsoft (Hotmail, Outlook, Windows Live etc.)
description: Microsoft är vanligtvis den näst största eller tredje största leverantören beroende på hur din lista är uppbyggd, och de hanterar trafik något annorlunda jämfört med andra Internet-leverantörer.
feature: null
topics: Deliverability
kt: 5319
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: f797faaf9189f64eb6fc57b84c5e38d4418d5f51
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# [!DNL Microsoft] ([!DNL Hotmail], [!DNL Outlook], [!DNL Windows Live]osv.)

[!DNL Microsoft] är vanligtvis den näst största eller tredje största leverantören beroende på hur listan är uppbyggd, och de hanterar trafik något annorlunda jämfört med andra Internet-leverantörer.

Här är några högdagrar:

## Vilka data är viktiga

[!DNL Microsoft] fokuserar på avsändarens rykte, klagomål, användarinteraktion och deras egen grupp med betrodda användare (kallas även Sender Reputation Data eller SRD) som de avfrågar för feedback.

## Vilka data finns tillgängliga?

[!DNL Microsoft]Med sitt eget rapporteringsverktyg för avsändare, [!DNL Smart Network Data Services] (SNDS), kan ni se mätvärden för hur mycket e-post ni skickar och hur mycket e-post som accepteras, liksom för klagomål och skräppostfällor. Tänk på att delade data är ett exempel och inte återspeglar exakta tal, men det är bäst att representera hur [!DNL Microsoft] vyer du är som avsändare. [!DNL Microsoft] lämnar ingen offentlig information om sin betrodda användargrupp, men dessa data är tillgängliga via [!DNL Return Path Certification] programmet mot en extra avgift.

## Avsändarens rykte

[!DNL Microsoft] har traditionellt fokuserat på att skicka IP i sina utvärderingar och filtreringsbeslut. De arbetar aktivt med att utöka sina funktioner för att skicka domäner. Båda drivs till stor del av de traditionella anseendepåverkarna, som klagomål och skräppostfällor. Leveransmöjligheterna kan också i hög grad påverkas av programmet för certifiering av returtåglägen, som har specifika kvantitativa och kvalitativa programkrav.

## Insikter

[!DNL Microsoft] kombinerar alla sina mottagande domäner för att etablera och spåra sändningens anseende. Detta inkluderar [!DNL Hotmail], [!DNL Outlook], MSN [!DNL Windows Live]och så vidare, liksom alla e-postmeddelanden som skickas via Office 365. [!DNL Microsoft] kan vara särskilt känslig för volymvariationer, så överväg att tillämpa specifika strategier för att öka och minska från stora sändningar i stället för att tillåta volymbaserade plötsliga förändringar.

[!DNL Microsoft] är också särskilt strikt under IP-värmarnas första dagar, vilket vanligtvis innebär att de flesta postmeddelanden filtreras först. De flesta internetleverantörer anser att avsändarna är oskyldiga tills de har bevisats skyldiga. [!DNL Microsoft] är motsatsen och ser dig skyldig tills du bevisar dig oskyldig.