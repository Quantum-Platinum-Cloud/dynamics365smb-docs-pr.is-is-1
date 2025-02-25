---
title: Viðbót grunnupplifunar | Microsoft Docs
description: Þessi viðbót er nútímalegur valkostur í stað Microsoft Dynamics C5.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'C5, financials, extension'
ms.search.form: '20600,'
ms.date: 04/01/2021
ms.author: bholtorf
---

# <a name="the-basic-experience-extension" />Viðbót grunnupplifunar

Ef þú hefur verið með Microsoft Dynamics C5 geta samstarfsaðilar Microsoft hjálpað þér að skipta yfir í nútímalega lausn sem byggir á [!INCLUDE[prod_short](includes/prod_short.md)], þannig að þú getir haldið áfram að njóta sömu einföldu möguleikana og Dynamics C5.

Þessi viðbót er ætluð fyrir lítil fyrirtæki og getur stutt við allt að þrjá notendur. Ef þörf er á fleiri notendum þarf að uppfæra í [!INCLUDE[prod_short](includes/prod_short.md)]-leyfi og fjarlægja þessa viðbót.

> [!NOTE]
> Eins og staðan er í dag er þessi viðbót aðeins í boði fyrir viðskiptamenn í Danmörku og á Íslandi.

## <a name="whats-available" />Hvað er í boði

Eftirfarandi tafla lýsir möguleikunum sem eru í boði ef viðbót grunnupplifunar er sett upp.

|Svæðarit  |Aðgerð  |
|---------|---------|
|**Fjárhagur** |Grunnfjármál, fjárhagsskýrslur, eignir, bankakerfi, bankaafstemming, greiðslur, beingreiðsla, víddir, margir gjaldmiðlar, fjárhagsáætlanir, verkflæði, skjalastjórnun/stafakennsl, sameining, ótakmörkuð fyrirtæki|
|**Viðskiptakröfur/sala** |Grunnviðskiptakröfur, reikningsfærsla sölu, söluafslættir, verðlagning, virðisaukaskattur, tengslastjórnun |
|**Viðskiptaskuldir/innkaup** |Grunnviðskiptaskuldir, reikningsfærsla innkaupa |
|**Verkefnastjórnun** |Verk, verðlagning verks, vinnuskýrslur, úthlutun, verkefni, tilföng |
|**Birgðir** |Grunnbirgðir, staðgenglar vörur, millivísun vöru |

## <a name="getting-started" />Hafist handa

Þessi viðbót er aðeins öðruvísi en flestar og þú þarft aðstoð frá samstarfsaðila Microsoft til að setja hana upp. Bara þannig að þú vitir hverju þú mátt búast við, þá er hér mikil yfirsýn yfir það hvað samstarfsaðili Microsoft mun gera.

1. Stofna nýjan [!INCLUDE[prod_short](includes/prod_short.md)] leigjanda. Þetta gæti verið annaðhvort prufuútgáfa eða útgáfa skýjalausnarveitu (CSP).
2. Bætið að minnsta kosti einum notanda við sem er úthlutað á leyfi grunnupplifunar á Azure Active Directory-reikningnum.
3. Fjarlægið öll fyrirtæki, þar á meðal sýnifyrirtækið Cronus.
4. Stofnið nýtt fyrirtæki sem inniheldur engin sýnigögn eða uppsetningar.
5. Bætið við **Sýniútgáfu RapidStart** pakkanum. <!--what does the package contain?-->
6. Sækið og setjið upp viðbót grunnupplifunar úr AppSource.

## <a name="migrating-data" />Gögn flutt

Komdu með Dynamics C5 gögnin þín. Þegar samstarfsaðili Microsoft hefur sett upp viðbót grunnupplifunar færðu tómt fyrirtæki í hendurnar. Auðveld leið til að yfirfæra gögnin úr Dynamics C5 í grunnupplifun er að nota viðbót gagnaflutnings fyrir C5 sem fylgir með í [!INCLUDE[prod_short](includes/prod_short.md)]. Viðbótin flytur viðskiptamenn, lánardrottna, vörur og fjárhagslykla og færslur þeirra.

## <a name="see-also" />Sjá einnig .

[C5-gagnaflutningsviðbótin](ui-extensions-c5-data-migration.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
