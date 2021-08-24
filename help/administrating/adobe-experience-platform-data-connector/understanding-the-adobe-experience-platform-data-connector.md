---
title: Förstå Adobe Experience Platform Data Connector
description: Adobe Experience Platform Data Connector hjälper befintliga kunder att göra sina data tillgängliga på Adobe Experience Platform genom att mappa XTK-data (data som importerats i Campaign) till Experience Data Model-data (XDM) på Adobe Experience Platform.
feature: Integrering av tjänsten People Core
kt: 2826
thumbnail: 27304.jpg
doc-type: feature video
activity: understand
team: TM
exl-id: 686961f9-5374-4cc6-8b36-7ee0584ea720
source-git-commit: 2ba22e7e7d193278fd06cb4b2dc80f650f754ec8
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 4%

---

# Förstå Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Funktionen är i betaversion och kan uppdateras ofta och ändras utan föregående meddelande.
>
>Kontakta [!UICONTROL Adobe Customer Support] om du tänker implementera den här funktionen.

## Översikt

Adobe Experience Platform [!UICONTROL Data Connector] hjälper befintliga kunder att göra sina data tillgängliga på Adobe Experience Platform genom att mappa XTK-data (data som importerats i Adobe Campaign) till [!DNL Experience Data Model] (XDM)-data på Adobe Experience Platform.

Kopplingen är enkelriktad och skickar data från Adobe Campaign Standard till Adobe Experience Platform. Data skickas aldrig från Adobe Experience Platform till Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] är avsett för datatekniker som förstår Adobe Campaign Standard [!UICONTROL custom resources] och har en förståelse för hur kundens övergripande dataschema ska vara inuti Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Den här videon ger en översikt över Adobe Experience Platform  [!UICONTROL Data Connector] (09:35 min)*

>[!NOTE]
>
>Det går inte att överföra [!UICONTROL subscription events] direkt. Om du vill överföra [!UICONTROL subscription events] kan du skapa motsvarande XDM och datauppsättning på Adobe Experience Platform och sedan konfigurera en anpassad datamappning för dessa data.
>
>Befintliga [!UICONTROL experience events] kan inte importeras till Adobe Experience Platform, men pågående [!UICONTROL experience events] som genereras direktuppspelas till Adobe Experience Platform.

## Viktiga steg för datamappning

I följande självstudier beskrivs de viktigaste stegen för att utföra en datamappning mellan Campaign Standard och Adobe Experience Platform:

1. [Mappa anpassade resurser](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Kartlägga upplevelsehändelser](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappa starttabelldata](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Ändra datamappningen](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Kontrollera status för ett datainmatningsjobb](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Ytterligare resurser

* [Om Adobe Experience Platform Data Connector](https://experienceleague.adobe.com/docs/campaign-standard/using/integrating-with-adobe-cloud/adobe-experience-platform/data-connector/aep-about-data-connector.html)

