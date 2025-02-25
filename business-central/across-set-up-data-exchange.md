---
title: Setja upp gagnaskipti til að senda og taka á móti skrám
description: Settu upp gagnaskiptaramma til að skiptast á gögnum við ytri skrár; til að senda og taka á móti rafrænum skjölum eða flytja inn og út bankaskrár.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/11/2021
ms.author: edupont
---
# <a name="setting-up-data-exchange" />Setja upp gagnaskipti

Áður en hægt er að senda og taka á móti rafrænum skjölum eða flytja inn og út bankaskrár verður að setja upp gagnaskiptaumgjörð til að vinna úr umræddum skjölum. Auk þess verður að setja upp tengd svæði, t.d. viðskiptamenn sem fá senda rafræna reikninga eða AMC Banking 365 Fundamentals-viðbótina í tilvikum þar sem nota þarf utanaðkomandi þjónustuaðila til að umbreyta bankaskrám. Frekari upplýsingar eru í [Rafræn gagnaskipti](across-data-exchange.md).  

 Þegar [!INCLUDE[prod_short](includes/prod_short.md)] er sett upp fyrir gagnaskipti við ytri skrár geta notendur notað uppsetningu í almennum viðskiptaverkum, s.s. að senda og taka á móti rafrænum skjölum og flytja inn og út bankaskrár.  

 Eftirfarandi tafla lýsir röð verkefna með tenglum í efnisatriði þar sem þeim er lýst.  

|**Til að**|**Sjá**|  
|------------|-------------|  
|Setja upp forstillta skjalaskiptaþjónustu til að hægt sé að senda og taka á móti rafrænum skjölum frá og til [!INCLUDE[prod_short](includes/prod_short.md)].|[Setja upp skjalaskiptaþjónustu](across-how-to-set-up-a-document-exchange-service.md)|  
|Setja upp forstillta OCR-þjónustu til að breyta PDF eða myndaskrár í rafræn skjöl sem hægt er að breyta í færslur fyrir skjöl í [!INCLUDE[prod_short](includes/prod_short.md)].|[Setja upp skjöl á innleið](across-how-setup-income-documents.md)|  
|Setja upp eina af tveimur forstilltum þjónustu til að fá nýjasta gengi gjaldmiðils á síðunni **Gengi gjaldmiðils**.|[Uppfæra gengi](finance-how-update-currencies.md)|  
|Setja upp mismunandi aðalgögn, t.d. upplýsingar um fyrirtækið, viðskiptavini, lánardrottna, atriði, og mælieiningar, sem tengjast vörpunargögnum í [!INCLUDE[prod_short](includes/prod_short.md)]|[Setja upp sendingu og móttöku rafrænna skjala](across-how-to-set-up-electronic-document-sending-and-receiving.md)|  
|Setja upp bankareikning, lánardrottin og greiðslubók fyrir SEPA-millifærslur.|[Setja upp SEPA-kreditfærslur](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md#setting-up-sepa-credit-transfer)|  
|Undirbúið bankareikningssnið, greiðsluaðferðir og samninga við viðskiptavini um SEPA-beingreiðslur.|[Innheimta greiðslur með SEPA-beingreiðslum](finance-collect-payments-with-sepa-direct-debit.md)|  
|Setja upp sannvottun notanda og vefslóð veitu AMC Banking 365 Fundamentals-viðbótarinnar sem er nauðsynleg til að umbreyta bankaskrám á snið bankans þíns.|[Nota AMC Banking 365 Fundamentals viðbótina](ui-extensions-amc-banking.md)|  
|Setja upp og virkja utanaðkomandi þjónustu sem gerir kleift að flytja inn bankayfirlit beint sem bankastreymi.|[Setja upp bankayfirlitsþjónustu](bank-how-setup-bank-statement-service.md)|  
|Eftir að bankayfirlitsþjónusta er gerð virk skal tengja bankareikninga í [!INCLUDE[prod_short](includes/prod_short.md)]|[Bankareikningar settir upp](bank-how-setup-bank-accounts.md)|  
|Settu upp gagnaútflutning fyrir Intrastat-skýrslugerð í [!INCLUDE[prod_short](includes/prod_short.md)].|[Setja upp Intrastat skýrslugerð](finance-how-setup-report-intrastat.md)|
|Undirbúið að setja upp nýja gagnaskiptaskilgreiningu fyrir tiltekna gagnaskrá eða straum með því að nota XML-skema skrárinnar til að fylla út í flýtiflipann **Dálkskilgreiningar** á síðunni **Bókunarskilgreining**.|[Nota XML-skema til að undirbúa skilgreiningar gagnaskipta](across-how-to-use-xml-schemas-to-prepare-data-exchange-definitions.md)|  
|Setja upp Data Exchange Framework til að gera notendum kleift að taka á móti nýju sniði innkaupaskjala, senda ný snið söluskjala, flytja inn nýjar bankaskrá eða önnur gagnaskipti.|[Setja upp skilgreiningar gagnaskipta](across-how-to-set-up-data-exchange-definitions.md)|  

## <a name="see-related-microsoft-trainingtrainingmoduleselectronic-documents-dynamics-365-business-central" />Sjá tengda [Microsoft þjálfun](/training/modules/electronic-documents-dynamics-365-business-central/)

## <a name="see-also" />Sjá einnig .

[Rafræn gagnaskipti](across-data-exchange.md)  
[Skjöl á innleið](across-income-documents.md)  
[Almenn viðskiptavirkni](ui-across-business-areas.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
