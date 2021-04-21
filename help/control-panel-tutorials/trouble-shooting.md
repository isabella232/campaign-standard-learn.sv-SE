---
title: Felsöka kontrollpanelen
description: Med kontrollpanelen kan du övervaka och hantera SFTP-lagringen per instans och tillåtslista IP-adresser.
feature: 'Kontrollpanelen  '
kt: 2938
doc-type: article
activity: use
team: PM
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
translation-type: tm+mt
source-git-commit: ada0b029245190f53d58fa93c79c161719bfe9fd
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 100%

---

# Felsöka [!UICONTROL Control Panel]

Läs mer om hur du felsöker problem med att använda kontrollpanelen.

## Logga in och hemsidan

Problem med att logga in och hemsidan.

### Symptom: det går inte att logga in på Adobe Experience Cloud

**Så här gör du:**
användaren måste hitta sitt [!DNL IMS Org ID] (xxx). Administratören måste lägga till användaren i [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] för varje instans som denne vill hantera. Om användaren är en administratör för alla instanser kan denne fortfarande behöva lägga till sig själv som *[!UICONTROL user]*.

### Symptom: länkarna i [!UICONTROL Adobe Experience Cloud Home] för åtkomst till [!UICONTROL Control Panel] visas inte för en användare

**Orsak:**
användarna ser inte länkarna förrän de läggs till som användare i [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**Så här gör du:**
Administratören måste lägga till användaren i [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* för varje instans som denne vill hantera. Om användaren är en administratör för alla instanser kan denne fortfarande behöva lägga till sig själv som *[!UICONTROL user]*.

### Symptom: en instans visas inte i [!UICONTROL Control Panel]

**Orsak:**
troligtvis måste användaren läggas till som en *[!UICONTROL user]* med produktprofil i `Campaign-xxx-Administrators/Admin` för den instans som saknas

**Så här gör du:**
Administratören måste lägga till användaren i produktprofilen i `Campaign-xxx-Admins` för varje instans som denne vill hantera. Om användaren är en administratör för alla instanser kan denne fortfarande behöva lägga till sig själv som *[!UICONTROL user]*.

### Användbara videor

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*Kontrollera [!DNL IMS Org ID] (00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*Så här lägger du till en administratör i [!UICONTROL product profile] [!DNL administrators] för att kunna använda [!UICONTROL Control Panel] (01:03 min)*

### Användbar dokumentation

* [Upptäck [!UICONTROL Control Panel]](https://helpx.adobe.com/se/campaign/kb/control-panel-overview.html)
* [Hantera behörigheter för [!UICONTROL Control Panel]](https://helpx.adobe.com/se/campaign/kb/control-panel-access.html)

## Upprätta en anslutning till en SFTP-server (klient eller API)

För anslutning till SFTP-servrar krävs:

* [!UICONTROL allow listing]-IP-adressen som används för anslutning till SFTP-servern
* ett privat/offentligt nyckelpar som måste registreras i Adobe Campaign
* Om du ansluter till SFTP-servern direkt behöver du även en SFTP-klientprogramvara

### Användbar dokumentation {#helpful-docs}

* [Logga in på SFTP-servern](https://docs.adobe.com/content/help/sv-SE/control-panel/using/control-panel-home.html#LoggingintoyourSFTPserver)
