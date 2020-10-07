---
title: Andra mätvärden som är viktiga för leveransen
description: Ett av de bästa sätten att identifiera ett utsändande anseendeproblem är genom mätvärdena. Låt oss titta på några viktiga mätvärden för leveransförmåga för att övervaka och använda dem för att identifiera ett problem med anseende.
feature: null
topics: Deliverability
kt: 5256
doc-type: article
activity: understand
team: TM
translation-type: tm+mt
source-git-commit: 6e4824185b84715d514bf21aace9e57c602e970d
workflow-type: tm+mt
source-wordcount: '1367'
ht-degree: 0%

---


# Andra mätvärden som är viktiga för leveransen

Ett av de bästa sätten att identifiera ett utsändande anseendeproblem är genom mätvärdena. Låt oss titta på några viktiga mätvärden för leveransförmåga för att övervaka och använda dem för att identifiera ett problem med anseende.

## studsar

Satser är resultatet av ett leveransförsök och fel där Internet-leverantören tillhandahåller meddelanden om misslyckanden. Hantering av studsar är en viktig del av listhygienen. När ett visst e-postmeddelande har studsat flera gånger i rad flaggas det för undertryckning i den här processen. Antalet och typen av studsar som krävs för att utlösa inaktiveringen varierar från system till system. Den här processen förhindrar att system fortsätter att skicka ogiltiga e-postadresser. Satser är en av de viktigaste data som internetleverantörer använder för att fastställa IP-anseendet. Det är mycket viktigt att hålla ett öga på denna mätmetod. &quot;Levererat&quot; jämfört med &quot;studsat&quot; är förmodligen det vanligaste sättet att mäta leveransen av marknadsföringsmeddelanden: Ju högre procenttal som levereras, desto bättre. Vi gräver in i två olika typer av studsar.

## Hårda studsar

Hårda studsar är permanenta fel som genereras efter att en Internet-leverantör har fastställt att ett postförsök till en prenumerantadress inte kan levereras. Inom Adobe Campaign läggs hårda studsar som kategoriseras som olevererbara till i karantänen, vilket betyder att de inte kommer att försökas igen. Det finns vissa fall där ett hårt studsande skulle ignoreras om orsaken till felet är okänd. Här är några vanliga exempel på hårda studsar:

* Adressen finns inte
* Kontot är inaktiverat
* Felaktig syntax
* Felaktig domän

## Mjuka studsar

Mjuka studsar är tillfälliga fel som internetleverantörer genererar när de har svårt att leverera e-post. Mjuka fel kommer att upprepas flera gånger (med olika variationer beroende på hur anpassade eller färdiga leveransinställningar för Adobe Campaign används) för att försöka leverera korrekt. Adresser som kontinuerligt mjuka studsar kommer inte att läggas till i karantän förrän det maximala antalet försök har gjorts (som återigen varierar beroende på inställningarna). Några vanliga orsaker till mjuka studsar är:

* Postlådan är full
* Tar emot e-postserver nedåt
* Problem med avsändarens rykte

![studstyper](assets/bounce-types.png)

>[!NOTE]
>
>Satser är en viktig indikator på ett renomméproblem eftersom de kan markera en dålig datakälla (hård studs) eller ett anseendeproblem med en Internet-leverantör (mjuk studsa).
>
>Mjuka studsar förekommer ofta som en del av e-postutskick och bör kunna lösas under återförsöksbearbetningen innan de karakteriseras som ett problem med äkta leverans. Om din låga avhoppsfrekvens är över 30 procent för en enskild Internet-leverantör och inte kan lösas inom 24 timmar är det en bra idé att kontakta din Adobe Campaign-konsult.

## Klagomål

Klagomål registreras när en användare anger att ett e-postmeddelande är oönskat eller oväntat. Den här prenumerationsåtgärden loggas vanligtvis antingen via prenumerantens e-postklient när de klickar på skräppostknappen eller via ett skräppostrapporteringssystem från en annan leverantör.

### ISP-klagomål

De flesta Internet-leverantörer på nivå 1 och vissa på nivå 2 erbjuder en skräppostrapporteringsmetod till sina användare eftersom avanmälnings- och avanmälningsprocesser tidigare har använts på ett skadligt sätt för att validera en e-postadress. Adobe Campaign får dessa klagomål via ISP FBL. Detta fastställs under konfigurationsprocessen för alla Internet-leverantörer som tillhandahåller FBL och gör det möjligt för Adobe Campaign att automatiskt lägga till e-postadresser som klagas på karantänregistret för att undertryckas. Inspikar i ISP-klagomål kan vara en indikator på dålig listkvalitet, mindre än optimala listinsamlingsmetoder eller svaga engagemangspolicyer. De märks också ofta när innehållet inte är relevant.

### Klagomål från tredje part

Det finns flera skräppostgrupper som tillåter skräppostrapportering på en bred nivå. Kompletterande mätvärden som används av dessa tredje parter används för att tagga e-postinnehåll för att identifiera skräppost. Processen kallas även fingeravtryck. Användare av dessa metoder för klagomål från tredje part sparar vanligtvis mer information om e-post, så de kan ha större effekt än andra klagomål om de inte besvaras.

>[!NOTE]
>
>Internetleverantörer samlar in klagomål och använder dem för att fastställa en avsändares allmänna anseende. Alla klagomål ska undertryckas och inte längre kontaktas så snabbt som möjligt och i enlighet med lokala lagar och förordningar.

## Skräppostsvällning

En skräppostsvällning är en adress som används för att identifiera ett otillåtet eller oombett e-postmeddelande. Det finns svällning för skräppost som hjälper till att identifiera e-post från bedrägliga avsändare eller avsändare som inte följer vedertagna standarder för e-postmarknadsföring. E-postadressen för skräppostsvällning publiceras vanligtvis inte och är nästan omöjlig att identifiera. Om du levererar e-post till skräppostsvällningar kan det påverka ditt rykte med varierande svårighetsgrad beroende på typen av svällning och Internet-leverantör. Läs mer om de olika typerna av skräppostsvällning i följande avsnitt.

### Återvunnen

Återvunna skräppostsvällningar är adresser som en gång var giltiga men som inte längre används. Ett viktigt sätt att hålla listorna så rena som möjligt är att regelbundet skicka e-post till hela listan och på lämpligt sätt utelämna utdragna e-postmeddelanden. Detta gör att övergivna e-postadresser kan sättas i karantän och inte längre kan användas.

I vissa fall kan en adress återvinnas inom 30 dagar. Att skicka regelbundet är en viktig aspekt av god listhygien, tillsammans med att regelbundet undertrycka inaktiva användare. Återengagemangskampanjer är vanligtvis en del av avancerade e-postmarknadsföringsprogram. Med den här kampanjstilen kan avsändaren försöka få tillbaka användare som annars inte längre skulle skickas med e-post.

### Typo

Ett stavfel är en adress som innehåller en felstavning eller ett fel. Detta inträffar ofta med kända felstavningar i viktiga domäner som [!DNL Gmail] (t.ex.: [!DNL gmail] är ett vanligt typo). Internet-leverantörer och andra blocklistoperatorer registrerar kända felaktiga domäner som ska användas som skräppostfälla för att identifiera spammare och mäta avsändarens hälsa. Det bästa sättet att förhindra skräppostsvällning är att använda en dubbel anmälningsprocess för listsamling.

### Pristin

En primär skräppostsvällning är en adress som inte har någon slutanvändare och som aldrig har haft någon slutanvändare. Det är en adress som skapades enbart för att identifiera skräppost. Det här är den mest effektiva typen av skräppostfälla eftersom det är praktiskt taget omöjligt att identifiera och skulle kräva en hel del arbete för att rensa från din lista. I de flesta svarta listor används statiska skräppostsvällningar för att lista okända avsändare. Det enda sättet att undvika att pristine spam traps infekterar din breda e-postlista för marknadsföring är att använda en dubbel anmälningsprocess för listsamling.

## Bulkar

Bulking är leveransen av e-post till skräppostmappen hos en Internet-leverantör. Den är identifierbar när en låg öppningshastighet än normalt (och ibland klickfrekvens) kombineras med en hög leveransfrekvens. Orsaken till varför e-postmeddelanden skickas varierar mellan olika Internet-leverantörer. I allmänhet krävs dock en flagga som påverkar utskickandet av rykte (till exempel listhygien) för att meddelanden ska placeras i mappen bulk. Det är en signal på att ryktet minskar, vilket är ett problem som måste korrigeras omedelbart innan det påverkar fler kampanjer. Samarbeta med er Adobe Campaign-konsult för att åtgärda eventuella problem som beror på er situation.

## Blockera

Ett block uppstår när skräppostindikatorerna når en egen Internet-leverantör och Internet-leverantören börjar blockera e-post (märkbart genom utskicksförsök) från en avsändare. Det finns olika typer av block. I allmänhet förekommer block som är specifika för en IP-adress, men de kan också förekomma på den sändande domänen eller entitetsnivån. För att lösa ett block krävs särskild expertis, så kontakta din Adobe Campaign-konsult för att få hjälp.

## Blacklisting

En svartlistning inträffar när en svartlistningshanterare från tredje part registrerar skräppostliknande beteende som är kopplat till en avsändare. Orsaken till en svart lista publiceras ibland av det svarta listpartiet. En lista är vanligtvis baserad på IP-adress, men i allvarligare fall kan det vara via IP-intervall eller till och med en sändande domän. För att lösa problem med svartlistning bör ni få support från er Adobe Campaign-konsult för att kunna lösa och förhindra ytterligare listningar. Vissa listor är mycket allvarliga och kan orsaka långvariga och svåra problem med anseendet. Resultatet av en svartlistning varierar beroende på svartlistan, men kan påverka leveransen av all e-post.

## Ytterligare resurser

* [Typ av leveransfel och orsaker](https://docs.adobe.com/content/help/en/campaign-standard/using/testing-and-sending/monitoring-messages/understanding-delivery-failures.html#delivery-failure-types-and-reasons)
