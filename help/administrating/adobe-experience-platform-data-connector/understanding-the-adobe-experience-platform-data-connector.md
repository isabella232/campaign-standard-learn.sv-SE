---
title: Förstå Adobe Experience Platform Data Connector
description: Adobe Experience Platform Data Connector hjälper befintliga kunder att göra sina data tillgängliga på Adobe Experience Platform genom att mappa XTK-data (data som importerats i Campaign) till Experience Data Model-data (XDM) på Adobe Experience Platform.
feature: Adobe Experience Platform Data Connector
topics: ACoP
kt: 2826
doc-type: feature video
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: cb5d5bc58137fd374eafe165c6ea13288a60d7db
workflow-type: tm+mt
source-wordcount: '343'
ht-degree: 4%

---


# Förstå Adobe Experience Platform [!UICONTROL Data Connector]

>[!NOTE]
>
>Funktionen är för närvarande i betaversion och kan uppdateras ofta och ändras utan föregående meddelande.
>
>Kontakta [!UICONTROL Adobe Customer Support] om du tänker implementera den här funktionen.

## Översikt

Adobe Experience Platform [!UICONTROL Data Connector] hjälper befintliga kunder att göra sina data tillgängliga på Adobe Experience Platform genom att mappa XTK-data (data som importerats i Adobe Campaign) till [!DNL Experience Data Model] (XDM)-data på Adobe Experience Platform.

Observera att kopplingen är enkelriktad och skickar data från Adobe Campaign Standard till Adobe Experience Platform. Data skickas aldrig från Adobe Experience Platform till Adobe Campaign Standard.

Adobe Experience Platform [!UICONTROL Data Connector] är avsett för datatekniker som förstår Adobe Campaign Standard [!UICONTROL custom resources] och har en förståelse för hur kundens övergripande dataschema ska vara inuti Adobe Experience Platform.

>[!VIDEO](https://video.tv.adobe.com/v/27304?quality=12)

*Den här videon ger en översikt över Adobe Experience Platform[!UICONTROL Data Connector](09:35 min)*

>[!NOTE]
>
>Det går inte att överföra direkt från [!UICONTROL subscription events] programmet. Om du vill överföra [!UICONTROL subscription events]kan du skapa motsvarande XDM och datauppsättning på Adobe Experience Platform och sedan konfigurera en anpassad datamappning för dessa data.
>
>Befintliga filer [!UICONTROL experience events] kan inte importeras till Adobe Experience Platform, men pågående genereringar [!UICONTROL experience events] kommer att strömmas till Adobe Experience Platform.

## Viktiga steg för datamappning

I följande självstudier beskrivs de viktigaste stegen för att utföra en datamappning mellan Campaign Standard och Adobe Experience Platform:

1. [Mappa anpassade resurser](/help/administrating/adobe-experience-platform-data-connector/mapping-custom-resources.md)
2. [Mapping Experience Events](/help/administrating/adobe-experience-platform-data-connector/mapping-experience-events.md)
3. [Mappa starttabelldata](/help/administrating/adobe-experience-platform-data-connector/mapping-seed-table-data.md)
4. [Ändra datamappningen](/help/administrating/adobe-experience-platform-data-connector/modifying-data-mapping.md)
5. [Kontrollera status för datainmatningsjobb](/help/administrating/adobe-experience-platform-data-connector/checking-status-of-data-ingestion-jobs.md)

## Ytterligare resurser

* [Om Adobe Experience Platform Data Connector](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-about-data-connector.html)
* [Översikt över Experience Data Model](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-data-model-overview.html)
* [Mappningsdefinition](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-definition.html)
* [Aktivera mappning](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-mapping-activation.html)
* [Utlösa datainmatning via API:er](https://docs.adobe.com/content/help/en/campaign-standard/using/administrating/mapping-campaign-and-aep-data/aep-triggering-data-ingestion.html)
