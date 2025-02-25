---
title: Hönnunarupplýsingar - Endurmat
description: Hægt er að endurmeta birgðir á grundvelli virðisgrundvallar sem endurspeglar nákvæmast birgðavirði.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-revaluation" />Hönnunarupplýsingar: Endurmat
Hægt er að endurmeta birgðir á grundvelli virðisgrundvallar sem endurspeglar nákvæmast birgðavirði. Einnig er hægt að bakfæra endurmat, þannig að kostnaður við seldar vörur(kostnaður seldra vara) sé rétt uppfærður fyrir vöru sem hefur þegar verið seld. Vörur sem nota hefðbundna aðferð kostnaðarútreiknings og hafa ekki verið reikningsfærðar að fullu er einnig hægt að endurmeta.  

Í [!INCLUDE[prod_short](includes/prod_short.md)] er eftirfarandi sveigjanleiki studdur varðandi endurmat:  

-   Endurmetanlegt magn er hægt að reikna fyrir allar dagsetningar, líka aftur í tímann.  
-   Fyrir vörur sem nota kostnaðarútreikninginn Staðlað eru áætlaðar kostnaðarfærslur hafðar með í endurmatinu.  
-   Birgðaminnkanir sem verða fyrir áhrifum af endurmati eru greindar.  

## <a name="calculating-the-revaluable-quantity" />Reikna endurreiknanlegt magn
 Endurmetanlegt magn er eftirstandandi magn í birgðum sem hægt er að endurmeta á tiltekinni dagsetningu. Það er reiknað sem summa magns fyrir fullreikningsfærðar birgðahöfuðbókarfærslur með sömu bókunardagsetningu eða eldri en endurmatsdagsetningin.  

> [!NOTE]  
>  Vörur sem nota hefðbundna aðferð kostnaðarútreiknings eru meðhöndlaðar á annan hátt við reikningu endurmetanlegs magns fyrir vöru, birgðageymslu og afbrigði. Magn og virði birgðahöfuðbókarfærslna sem ekki hafa verið að fullu reikningsfærðar eru teknar með í endurverðmetanlega magninu.  

Eftir bókun endurmats er hægt að bóka birgðaaukningu eða -minnkun með bókunardagsetningu sem er á eftir bókunardagsetningu endurmats. Hins vegar hefur endurmat ekki áhrif á þetta magn. Til að halda jafnvægi á birgðum, aðeins upprunalega endurmetanlegt magn er talið.  

Vegna endurmats hægt að gera á hvaða degi, verður þú að hafa samninga um þegar hluturinn er talinn hluti af birgðum frá fjárhagslegum sjónarhóli. Til dæmis hvenær vara er í birgðum og hvenær varan er verk í vinnslu (VÍV).  

### <a name="example" />Dæmi
Eftirfarandi dæmi sýnir þegar VÍV-vara verður hluti birgða. Dæmið er byggt á við framleiðsluna á keðja með 150 tenglum.  

![VÍV birgðir og endurmat.](media/design_details_inventory_costing_10_revaluation_wip.png "VÍV birgðir og endurmat")  

**1Q**: Notandinn bókar innkaupatenglana sem móttekna. Eftirfarandi tafla sýnir afleidda birgðafærslu.  

|Bókunardags.|Vara|Tegund færslu|Magn|Færslunr.|  
|------------------|----------|----------------|--------------|---------------|  
|01-01-20|TENGILL|Innkaup|150|1|  

> [!NOTE]  
>  Nú er vara sem notar hefðbundna aðferð kostnaðarútreiknings í boði fyrir endurmat.  

**1V**: Notandinn bókar innkaupatengla sem reikningsfærða og tenglarnir verða hluti birgða, fjárhagslega séð. Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

|Bókunardags.|Tegund færslu|Dagsetning mats|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Beinn kostnaður|01-01-20|150,00|1|1|  

 **2Q + 2 V**: Notandinn bókar innkaupatengla sem notaða í framleiðslu járnkeðju. Fjárhagslega séð verða tenglarnir hluti af birgðum VÍV.  Eftirfarandi tafla sýnir afleidda birgðafærslu.  

|Bókunardags.|Vara|Tegund færslu|Magn|Færslunr.|  
|------------------|----------|----------------|--------------|---------------|  
|02-01-20|TENGILL|Notkun|-150|1|  

Eftirfarandi tafla sýnir afleidda virðisfærslu.  

|Bókunardags.|Tegund færslu|Dagsetning mats|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|02-01-20|Beinn kostnaður|02-01-20|-150,00|2|2|  

Virðisdagsetningin er stillt á dagsetningu bókunar fyrir notkun (02-01-20) sem regluleg birgðaminnkun.  

**3Q**: Notandinn bókar keðjuna sem frálag og lokar framleiðslupöntuninni. Eftirfarandi tafla sýnir afleidda birgðafærslu.  

|Bókunardags.|Vara|Tegund færslu|Magn|Færslunr.|  
|------------------|----------|----------------|--------------|---------------|  
|02-15-20|KEÐJA|Frálag|1|3|  

**3V**: Notandinn keyrir runuvinnsluna **Leiðrétta kostnað - Birgðafærslur**, sem bókar keðjuna sem reikningsfærða tila ð sýna að öll efnisnotkun hefur verið reikningsfærð að fullu. Fjárhagslega séð eru tenglarnir ekki lengur hluti af birgðum VÍV þegar frálagið er reikningsfært og jafnað að fullu. Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

|Bókunardags.|Tegund færslu|Dagsetning mats|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|------------------|----------------|--------------------|----------------------------|---------------------------|---------------|  
|01-15-20|Beinn kostnaður|01-01-20|150,00|2|2|  
|02-01-20|Beinn kostnaður|02-01-20|-150,00|2|2|  
|02-15-20|Beinn kostnaður|02-15-20|150,00|3|3|  

## <a name="expected-cost-in-revaluation" />Áætlaður kostnaður í endurmati
Endurmetanlegt magn er reiknað sem summa magns fyrir fullreikningsfærðar birgðahöfuðbókarfærslur með sömu bókunardagsetningu eða eldri en endurmatsdagsetningin. Þetta þýðir að þegar sumar vörur eru móttekin / flutt en ekki reikningfærðar er ekki hægt að reikna birgðavirði þeirra. Vörur sem nota hefðbundna aðferð kostnaðarútreiknings eru ekki takmarkaðar að þessu leyti.  

> [!NOTE]  
>  Önnur gerð áætlaðs kostnaðar sem hægt er að endurmeta eru VÍV-birgðir, eftir tilteknum reglum. Frekari upplýsingar eru í [VÍV endurmat á birgðum](design-details-revaluation.md#wip-inventory-revaluation).  

Við útreikning á endurreiknanlegu magni fyrir vörur sem nota staðlaða aðferð kostnaðarútreiknings eru teknar með birgðahöfuðbókarfærslur sem hafa ekki verið alveg innheimtar. Færslurnar eru þá endurmetnar þegar endurmatið er bókað. Þegar þú reikningsfærir endurmetnu færsluna eru eftirfarandi virðisfærslur stofnaðar:  

-   Vanaleg virðisdagsetning reikningsins með færslugerðinni **Beinn kostnaður**. Kostnaðurupphæð á þessari færslu er bein kostnaður frá upptökum línu.  
-   Virðisfærsla með færslugerðinni **Frávik**. Þessi færsla skráir muninn milli reikningsfærðs kostnaðar og endurmetins staðalkostnaðar.  
-   Virðisfærsla með færslugerðinni **Endurmat**. Þessi færsla sýnir bakfærslu á endurmati væntanlegs kostnaðar.  

### <a name="example" />Dæmi
Eftirfarandi dæmi, sem byggir á framleiðslu á keðju í síðasta dæmi, sýnir hvernig þrjár tegundir af færslum eru búnar til. Þetta er byggt á eftirfarandi atburðarás:  

1.  Notandinn bókar innkaupatenglana samkvæmt móttöku með einingakostnaði upp á SGM 2.00.  
2.  Notandinn bókar endurmat tenglanna með nýju einingaverði upp á SGM 3.00 sem uppfærir staðalkostnað í SGM 3.00.  
3.  Notandinn bókar upprunaleg kaup tenglanna samkvæmt reikningi, sem býr til eftirfarandi:  

    1.  Reikningsfærð virðisfærsla með færslugerð **Beinn kostnaður**.  
    2.  Virðisfærsla með færslugerð **Endurmat** til að skrá bakfærslu endurmats áætlaðs kostnaðar.  
    3.  Virðisfærsla með færslugerðinni Frávik, skráir mismun milli reikningsfærðs kostnaðar og endurmetins staðalkostnaðar.  
Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

|Skref|Bókunardags.|Tegund færslu|Dagsetning mats|Kostnaðarupphæð (væntanl.)|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|----------|------------------|----------------|--------------------|------------------------------|----------------------------|---------------------------|---------------|  
|1.|01-15-20|Beinn kostnaður|01-15-20|300,00|0,00|1|1|  
|2.|01-20-20|Endurmat|01-20-20|150,00|0,00|1|2|  
|3.a.|01-15-20|Beinn kostnaður|01-15-20|-300,00|0,00|1|3|  
|3.b.|01-15-20|Endurmat|01-20-20|-150,00|0,00|1|4|  
|3.c.|01-15-20|Frávik|01-15-20|0.00|450,00|1|5|  

## <a name="determining-whether-an-inventory-decrease-is-affected-by-revaluation" />Ákvarðað hvort birgðaminnkun verður fyrir áhrifum af endurmati
Dagsetning bókunar eða endurmats er notað til að ákvarða hvort birgðaminnkun verður fyrir áhrifum af endurmati.  

Eftirfarandi tafla sýnir skilyrði sem eru notuð fyrir vöru sem ekki notar meðalkostnaðarmatsaðferð.  

|Aðstæður|Færslunr.|Tímasetning|Verða fyrir áhrifum af endurmati|  
|--------------|---------------|------------|-----------------------------|  
|A|Fyrr en endurmatsfærslunúmer|Fyrr en bókunardagsetning endurmats|Nei|  
|B|Fyrr en endurmatsfærslunr.|Jafnt bókunardagsetningu endurmats|Nei|  
|C|Fyrr en endurmatsfærslunr.|Síðar en bókunardagsetning endurmats|Já|  
|D|Síðar en endurmatsfærslu nr.|Fyrr en bókunardagsetning endurmats|Já|  
|Villa|Síðar en endurmatsfærslu nr.|Jafnt bókunardagsetningu endurmats|Já|  
|F|Síðar en endurmatsfærslu nr.|Síðar en bókunardagsetning endurmats|Já|  

### <a name="example" />Dæmi
Eftirfarandi dæmi, sem sýnir endurmat vöru sem notar FIFO-kostnaðarmatsaðferð, er byggt á eftirfarandi atburðarás:  

1.  01-01-20 bókar notandinn innkaup sex eininga.  
2.  02-01-20 bókar notandinn sölu einnar einingar.  
3.  Á 03-01-20 bókar notandinn sölureikning fyrir 1 einingu  
4.  Á 04-01-20 bókar notandinn sölureikning fyrir 1 einingu  
5.  03-01-20 reiknar notandinn birgðavirði fyrir vöruna og bókar endurmat á kostnaðarverði vörunnar úr SGM 10,00 í SGM 8,00.  
6.  02-01-20 bókar notandinn sölu einnar einingar.  
7.  Á 03-01-20 bókar notandinn sölureikning fyrir 1 einingu  
8.  Á 04-01-20 bókar notandinn sölureikning fyrir 1 einingu  
9. Runuvinnslan **Leiðr. kostnað - Birgðafærslur** er keyrð.  

Eftirfarandi tafla sýnir afleiddar virðisfærslur.  

|Aðstæður|Bókunardags.|Tegund færslu|Dagsetning mats|Virt magn|Kostnaðarupphæð (raunverul.)|Birgðafærslunr.|Færslunr.|  
|--------------|------------------|----------------|--------------------|---------------------|----------------------------|---------------------------|---------------|  
||01-01-20|Innkaup|01-01-20|6|60,00|1|1|  
||03-01-20|Endurmat|03-01-20|4|-8,00|1|5|  
|A|02-01-20|Sala|02-01-20|-1|-10,00|2|2|  
|B|03-01-20|Sala|03-01-20|-1|-10,00|3|3|  
|C|04-01-20|Sala|04-01-20|-1|-10,00|4|4|  
||04-01-20|Sala|04-01-20|-1|2,00|4|9|  
|D|02-01-20|Sala|03-01-20|-1|-10,00|5|6|  
||02-01-20|Sala|03-01-20|-1|2,00|5|10|  
|Villa|03-01-20|Sala|03-01-20|-1|-10,00|6|7|  
||03-01-20|Sala|03-01-20|-1|2,00|6|11|  
|F|04-01-20|Sala|04-01-20|-1|-10,00|7|8|  
||04-01-20|Sala|04-01-20|-1|2,00|7|12|  

## <a name="wip-inventory-revaluation" />VÍV endurmat á birgðum
Endurmat VÍV-birgða felst í að endurmeta íhluti sem eru skráðir sem hluti af VÍV-birgðum á þeim tíma af endurmati.  

Sé það haft í huga er mikilvægt að koma á fót hefðum um það hvenær vara telst vera hluti af VÍV-birgðum frá fjárhagslegu sjónarmiði. Í [!INCLUDE[prod_short](includes/prod_short.md)], er til eftirfarandi hefð:  

-   Keyptur íhlutur verður hluti af hráefnisbirgðum frá bókun innkaupa sem reikningsfærðra.  
-   Keyptur/hálfsamsettur íhlutur verður hluti VÍV-birgða frá bókun notkunar hans í tengslum við framleiðslupöntun.  
-   Keyptur/hálfsamsettur íhlutur er áfram hluti VÍV-birgða þar til framleiðslupöntun (framleidd vara) er reikningsfærð.  

Það hvernig virðisdagsetningin fyrir virðisfærslu notkunar er stillt fylgir sömu reglum og fyrir birgðir sem ekki eru VÍV. Frekari upplýsingar eru í [Ákvarðað hvort birgðaminnkun verður fyrir áhrifum af endurmati](design-details-revaluation.md#determining-whether-an-inventory-decrease-is-affected-by-revaluation).  

VÍG-birgðir er hægt að endurmeta svo framarlega sem endurmatsdagsetningin er ekki eftir bókunardagsetningu samsvarandi birgðabókarfærslna af gerðinni Notkun og svo fremi sem samsvarandi framleiðslupöntun hefur ekki enn verið reikningsfærð.  

> [!CAUTION]  
>  Skýrslan um **Verðmæti birgða VÍV** sýni virði færlsna fyrir bókaðar framleiðslupantanir og geta því verið ruglingslegar fyrir WIP-vörur sem hafa verið endurmetnar.  

## <a name="see-also" />Sjá einnig
 [Hönnunarupplýsingar: Birgðakostnaður](design-details-inventory-costing.md)   
 [Hönnunarupplýsingar: Aðferð kostnaðarútreiknings](design-details-costing-methods.md)   
 [Hönnunarupplýsingar: Birgðavirði](design-details-inventory-valuation.md) [Stjórna birgðakostnaði](finance-manage-inventory-costs.md)  
 [Fjármál](finance.md)  
 [Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
