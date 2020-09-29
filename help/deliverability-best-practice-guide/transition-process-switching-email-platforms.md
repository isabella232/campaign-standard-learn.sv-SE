---
title: Övergångsprocess - Byta e-postplattform
description: 'När du flyttar ESP:er (e-postleverantörer) är det inte möjligt att även övergå befintliga, etablerade IP-adresser. Det är viktigt att ni följer bästa praxis för att utveckla ett positivt rykte när ni börjar om på nytt. Eftersom de nya IP-adresserna som du kommer att använda ännu inte har något anseende kan internetleverantörerna inte lita fullständigt på den post som kommer från dem och måste vara försiktiga med vad de tillåter att de levereras till sina kunder. '
feature: null
topics: Deliverability
kt: null
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: f4dbccc1fea3db4dbddec0d4329b359993b62d20
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Övergångsprocess - Byta e-postplattform

När du flyttar ESP:er (e-postleverantörer) är det inte möjligt att även övergå befintliga, etablerade IP-adresser. Det är viktigt att ni följer bästa praxis för att utveckla ett positivt rykte när ni börjar om på nytt. Eftersom de nya IP-adresserna som du kommer att använda ännu inte har något anseende kan internetleverantörerna inte lita fullständigt på den post som kommer från dem och måste vara försiktiga med vad de tillåter att de levereras till sina kunder.

Tänk på vad du gör när du träffar någon ny. Vanligtvis måste du bygga upp förtroende i stället för att lita på dem direkt. Tro inte att ert varumärke automatiskt kommer att hjälpa till med det förtroendet, eftersom skräppost kommer att använda ditt namn för att göra dåliga saker. Internetleverantörer måste omvärdera era sändningsmetoder eftersom de är mest påfallande när det gäller e-postleverans.

Att skapa ett gott rykte är en process. Men när det väl är fastställt kommer små negativa indikatorer att ha mindre betydelse för er och era postutskick.

![Övergångsprocessen](assets/transition-process.png)

Hur lång tid det tar att värma upp dina IP-adresser och domäner kan variera, men upp till åtta veckors test är vanligt för vanliga avsändare att etablera ett anseende hos de flesta Tier 1-internetleverantörer ([!DNL Gmail], [!DNL Microsoft], [!DNL Verizon]/[!DNL Yahoo]/[!DNL AOL]osv.).
I nästa avsnitt kommer vi att undersöka några nyckelområden som vi ska fokusera på att ta med oss på rätt sätt.

## Infrastruktur

Framgångsrik leverans är beroende av en stark grund. E-postinfrastruktur är en viktig del. En korrekt konstruerad e-postinfrastruktur innehåller flera komponenter - nämligen domän(er) och IP-adress(er). De här komponenterna är som maskinerna bakom de e-postmeddelanden du skickar, och de är ofta navet för att skicka rykte. Konsulter för slutprodukter ser till att dessa element är korrekt konfigurerade under implementeringen, men på grund av anseendeelementet är det viktigt att du har den här grundläggande förståelsen.

### Domäninställningar och -strategi

Tiderna har ändrats, och vissa Internet-leverantörer (som [!DNL Gmail] och [!DNL Yahoo]liknande) lägger nu in domänens anseende som en extra poäng när det gäller att knyta e-postens anseende till en avsändare. Ditt domänrykte baseras på din avsändande domän i stället för på din IP-adress. Detta innebär att ert varumärke har företräde när det gäller beslut om filtrering av Internet-leverantörer.

En del av introduktionsprocessen för nya avsändare på Adobe Campaign är bland annat att konfigurera dina sändande domäner och se till att din infrastruktur är korrekt etablerad. Du bör samarbeta med en expert om vilka domäner du tänker använda på lång sikt. Här följer några tips som utgör en bra domänstrategi:

* Var så tydlig och reflekterande som möjligt av varumärket med den domän du väljer, så att användarna inte felaktigt identifierar posten som skräppost. Några exempel är [!DNL newsletter.foo.com], [!DNL receipts.foo.com]och så vidare.
* Du bör inte använda din förälder eller företagsdomän eftersom det kan påverka leveransen av post från organisationen till Internet-leverantörer.
* Använd en underdomän till din överordnade domän för att legitimera den sändande domänen.
* Skilj era underdomäner åt för transaktions- och marknadsföringsmeddelandekategorier. Detta gör att e-posttrafiken kan flöda på ett mer tillförlitligt sätt eftersom internetleverantörer letar efter den här sändningsmetoden, som är en känd e-postmetod och som rekommenderas varmt.

### IP-strategi

Det är viktigt att utforma en välstrukturerad IP-strategi för att skapa ett gott rykte. Antalet IP-adresser och inställningar varierar beroende på er affärsmodell och era marknadsföringsmål. Samarbeta med en expert för att ta fram en tydlig strategi för att komma igång. Tänk på följande saker som är viktiga att tänka på:

* Alltför många IP-adresser kan utlösa anseendeproblem eftersom det är en vanlig taktik hos skräppost som används av skräppost, som används av skräppost där trafiken sprids över många IP-adresser för att maximera leveransen av skräppost. Även om du inte är skräppost kan du se ut som en om du använder för många IP-adresser, särskilt om dessa IP-adresser inte har haft någon tidigare trafik.
* Alltför få IP-adresser kan orsaka genomströmningsproblem och kan ge upphov till problem med anseendet. Dataflödet varierar beroende på Internet-leverantör. Hur mycket och hur snabbt en Internet-leverantör är villig att acceptera baseras vanligtvis på sin infrastruktur och sina anseendetrösklar.
* Det är viktigt att separera trafiken för meddelandetyper. Det är viktigt att ni, åtminstone, har separat marknadsföring och transaktionell e-post på separata IP-pooler.
* Beroende på er e-poststrategi kan det även vara tillrådligt att separera olika produkter eller marknadsföringsströmmar från olika IP-pooler om ert rykte är drastiskt annorlunda. Vissa marknadsförare segmenterar också efter region. Att separera IP-adressen för trafik med lägre anseende löser inte problemet med anseende, men det förhindrar problem med e-postleveranser med gott anseende. Ni vill trots allt inte offra er goda publik för en mer riskfylld.

### Feedback-slingor

Bakom kulisserna bearbetar Adobe Campaign data om studsar, klagomål, avbeställningar med mera. Inställningarna av dessa feedbackslingor är en viktig del av leveransen. Klaganden kan skada ett anseende, så du bör ta bort e-postadresser som registrerar klagomål från målgruppen. Det är viktigt att komma ihåg att dessa data [!DNL Gmail] inte returneras. Avsändningsrubriker och interaktionsfiltrering är särskilt viktiga för [!DNL Gmail] prenumeranter som nu har större delen av abonnentdatabaserna.

### Autentisering

Autentisering är den process som Internet-leverantörer använder för att validera en avsändares identitet. De två vanligaste autentiseringsprotokollen är [!DNL Sender Policy Framework (SPF)] och [!DNL DomainKeys Identified Mail] (DKIM). Dessa är inte synliga för slutanvändaren, men hjälper Internet-leverantörer att filtrera e-post från verifierade avsändare. [!DNL Domain-based Message Authentication Reporting and Conformance] (DMARC) blir allt populärare, även om dess policyer ännu inte införlivats av alla internetleverantörer i deras anseende.

#### **SPF**

[!DNL Sender Policy Framework (SPF)] är en autentiseringsmetod som gör att ägaren till en domän kan ange vilka e-postservrar som de använder för att skicka e-post från den domänen.

#### **DKIM**

[!DNL Domain Keys Identified Mail (DKIM)] är en autentiseringsmetod som används för att identifiera förfalska avsändaradresser (kallas ofta [!DNL spoofing]). Om DKIM är aktiverat kan mottagaren bekräfta om avsändaren har behörighet att skicka e-post från den domänen.

#### **DMARC**

[!DNL Domain-based Message Authentication, Reporting and Conformance (DMARC)] är en autentiseringsmetod som ger domänägare möjlighet att skydda sin domän mot obehörig användning. DMARC använder SPF eller DKIM eller båda för att tillåta en domänägare att kontrollera vad som händer med e-post som inte kan autentiseras: levererat, i karantän eller avvisat.

## Målkriterier

När du skickar ny trafik bör du endast rikta dig till dina högst engagerade användare under de tidiga faserna av IP-uppvärmningen. Detta bidrar till att etablera ett gott rykte från start till mål och bygga upp förtroende innan ni rullar in era mindre engagerade målgrupper. Här är en grundformel för engagemang:

![Formel för registrering](assets/formula-for-enagement.png)

Normalt baseras en engagemangsfrekvens på en viss tidsperiod. Mätvärdet kan variera drastiskt beroende på om formeln används på en övergripande nivå eller för specifika posttyper eller kampanjer. De specifika målinriktningskriterierna måste tillhandahållas genom att ni samarbetar med er Adobe Campaign-konsult, eftersom alla avsändare och Internet-leverantörer varierar och vanligtvis behöver en skräddarsydd plan.

## ISP-specifika överväganden under IP-uppvärmning

Internetleverantörer har olika regler och olika sätt att se på sin trafik. Exempelvis [!DNL Gmail] är en av de mest avancerade internetleverantörerna eftersom de tittar mycket strikt på engagemang (öppningar och klick) utöver alla andra kända åtgärder. Detta kräver en anpassad plan som endast riktar sig till de mest engagerade användarna vid starten. Andra Internet-leverantörer kan kräva samma sak. Samarbeta med er Adobe Campaign-konsult för ett specifikt avtal.

## Volym

Mängden post som du skickar är avgörande för att vi ska få ett gott rykte. Ställ dig själv i en Internet-leverantörs skor - om du börjar se en massa trafik från någon du inte vet skulle det vara alarmerande. Det är riskabelt att skicka stora mängder post direkt och det kommer troligen att orsaka problem med anseendet som ofta är svåra att lösa. Det kan vara frustrerande, tidskrävande och kostsamt att gräva sig ur dåligt rykte och bränna och blockera problem som uppstår när man skickar för mycket för tidigt.

Volymtröskeln varierar mellan olika Internet-leverantörer och kan också variera beroende på era genomsnittliga engagemangsmått. Vissa avsändare kräver en mycket låg och långsam volymavgång, medan andra kan tillåta en brantare volymavgång. Vi rekommenderar att du arbetar med en expert, som en Adobe Campaign-konsult, för att ta fram en skräddarsydd volymplan.

Här är en lista med tips och tips för hur du smidigt kan övergå till nästa steg:

* **Behörighet** är grunden för alla framgångsrika e-postprogram.
* **Låg och långsam start** med låga sändningsvolymer och öka sedan i takt med att du bekräftar ditt avsändarrykte.
* Med en strategi **för** tandem-utskick kan ni öka volymen på Campaign samtidigt som ni sluter er med er nuvarande ESP, utan att störa er e-postkalender.
* **Engagemangsfrågor** - börja med de prenumeranter som öppnar och klickar på dina e-postmeddelanden regelbundet.
* **Följ planen** - våra rekommendationer har hjälpt hundratals Campaign-kunder att förbättra sina e-postprogram.
* **Övervaka ditt e-postkonto** för svar. Det är en dålig upplevelse för kunden att använda [!DNL nore-ply@xyz.com] eller inte svara.
* Inaktiva adresser kan ha negativ påverkan på leveransen. **Återaktivera och återge behörigheter** på din nuvarande plattform, inte på dina nya IP-adresser.
* **Domäner** - använd en sändande domän som är en underdomän till företagets faktiska domän. Om din företagsdomän till exempel är [!DNL xyz.com], [!DNL email.xyz.com] ger Internet-leverantörerna större trovärdighet än [!DNL xyzemail.com]
* **Genomskinlighet** - registreringsinformation för din e-postdomän ska vara tillgänglig för allmänheten och inte vara privat.

I många fall följer inte transaktionsmarknadsföring den traditionella uppvärmningsmetoden. Det är uppenbart svårt att styra volymen i transaktionsmejl på grund av dess natur, eftersom det i allmänhet krävs en användarinteraktion för att utlösa e-postberöringen. I vissa fall kan transaktionsmejl enkelt överföras utan en formell plan. I andra fall kan det vara bättre att övergå varje meddelandetyp över tiden för att sakta utöka volymen. Du kan till exempel använda följande övergångar:

1. Inköpsbekräftelser - generellt högt engagemang
2. Avbruten kundvagn - medelhögt engagemang i allmänhet
3. Välkomstmeddelanden - hög engagemangsnivå men kan innehålla felaktiga adresser beroende på vilka listsamlingsmetoder du använder
4. Återkommande e-postmeddelanden - generellt lägre engagemang

## Ytterligare resurser

* [Starta en ny plattform](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/managing-deliverability/starting-new-platform.html)
