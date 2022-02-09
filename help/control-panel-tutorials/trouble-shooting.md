---
title: Felsöka kontrollpanelen
description: På Kontrollpanelen kan du övervaka och hantera SFTP-lagringen per instans och tillåtslista IP-adresser.
feature: Control Panel
kt: 2938
doc-type: article
activity: use
team: PM
recommendations: noDisplay
exl-id: f546f791-a69b-4586-abfa-3e626b8feb17
source-git-commit: 57dbf456625d22cd2e4526d92e5a8c20a048d339
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 47%

---

# Felsöka [!UICONTROL Control Panel]

Läs mer om hur du felsöker problem med att använda kontrollpanelen.

## Logga in och hemsidan

Problem med att logga in och hemsidan.

### Symptom: Det går inte att logga in på Adobe Experience Cloud

**Så här gör du:**
Användaren måste hitta sina [!DNL IMS Org ID] (xxx). Administratören måste lägga till användaren i [!UICONTROL product profile] [!DNL “Campaign-xxx-Admins”] för varje instans som de vill hantera. Om användaren är administratör för alla instanser måste de lägga till sig själva som *[!UICONTROL user]*.

### Symptom: länkarna i [!UICONTROL Adobe Experience Cloud Home] för åtkomst till [!UICONTROL Control Panel] visas inte för en användare

**Orsak:**
användarna ser inte länkarna förrän de läggs till som användare i [!UICONTROL product profile] `Campaign-xxx-Administrators/Admin`

**Så här gör du:**
Administratören måste lägga till användaren i [!UICONTROL product profile] *[!DNL Campaign-xxx-Admins]* för varje instans som de vill hantera. Om användaren är administratör för alla instanser måste de lägga till sig själva som *[!UICONTROL user]*.

### Symptom: En instans visas inte i [!UICONTROL Control Panel]

**Orsak:**
Den mest troliga användaren måste läggas till som *[!UICONTROL user]* Produktprofil `Campaign-xxx-Administrators/Admin` för instansen som saknas

**Så här gör du:**
Administratören måste lägga till användaren i produktprofilen `Campaign-xxx-Admins` för varje instans som de vill hantera. Om användaren är administratör för alla instanser måste de lägga till sig själva som *[!UICONTROL user]*.

### Användbara videor

>[!VIDEO](https://video.tv.adobe.com/v/27183?quality=12)

*Kontrollera [!DNL IMS Org ID] (00:26 min)*

>[!VIDEO](https://video.tv.adobe.com/v/27147?quality=12)

*Så här lägger du till en administratör i [!UICONTROL product profile] [!DNL administrators] för att kunna använda [!UICONTROL Control Panel] (01:03 min)*

### Användbar dokumentation

* [Upptäck [!UICONTROL Control Panel]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=sv)
* [Hantera behörigheter för [!UICONTROL Control Panel]](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)

## Upprätta en anslutning till en SFTP-server (klient eller API)

För anslutning till SFTP-servrar krävs:

* [!UICONTROL allow listing]-IP-adressen som används för anslutning till SFTP-servern
* Ett privat/offentligt nyckelpar som måste registreras i Adobe Campaign
* Om du ansluter till SFTP-servern direkt behöver du SFTP-klientprogramvara

### Användbar dokumentation {#helpful-docs}

* [Logga in på SFTP-servern](https://experienceleague.adobe.com/docs/control-panel/using/control-panel-home.html?lang=en)
