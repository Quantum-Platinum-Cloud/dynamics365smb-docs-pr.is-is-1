---
title: Af hverju er síða læst og því ekki hægt að sérsníða hana
description: Það gæti verið lokað á þig að sérsníða síðu. Lestu hér um hvað þú getur gert til að opna á það svo þú getir sérstillt hana.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'customize, personalize, personalization, hide columns, remove fields, move fields'
ms.search.form: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="why-a-page-is-locked-from-personalization" />Af hverju er síða læst og því ekki hægt að sérsníða hana

Það eru tvö skilyrði sem koma í veg fyrir að þú sérsníðir síðu. Annaðhvort er síðan læst (eins og kemur fram í ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") tákninu) eða hún er útilokuð (eins og kemur fram í ![Sérstilling útilokuð.](media/personalization-blocked-icon.png "Sérstilling útilokuð") tákninu).

## <a name="locked-from-personalizing" />Læst fyrir sérstillingar

Ef það er ![Sérstillingarlás.](media/personalization-lock-icon.png "Sérstilla lás") tákn á borðanum **Sérstilling** þegar síða er opnuð merkir það að þú getir ekki gert frekari breytingar á sérstillingu síðunnar.

<!-- This is because we changed the way personalization works behind the scenes since the last time that you personalized the page. Unfortunately, the old way and new of doing things do not work together.

The page currently includes the last personalization changes that you made. If you want to continue personalizing the page, then you can choose the lock icon and then **Unlock**. Just be aware that if you choose to unlock the page, the current personalization of the page will be cleared, and you will have to start from scratch.
-->

Tvær ástæður koma til greina:

1. Þú hefur sérstillt síðuna áður, en það var gert með eldri útgáfu af vörunni. Við breyttum því hvernig sérstilling virkar frá því að þú sérstilltir síðuna síðast. Því miður vinna gamla og nýja aðferðin ekki saman.

2. Fram að þessu hefur þú aðeins notað bogann sem er úreltur [!INCLUDE[nav_windows_md](includes/nav_windows_md.md)] til að sérsníða síðuna.

### <a name="unlocking-the-page" />Síða aflæst

Ef þú vilt taka síðu úr lás og halda áfram að sérstilla hana skaltu velja táknið ![Sérstilla lás](media/personalization-lock-icon.png "Sérstilla lás") og síðan aðgerðina **Taka úr lás**.  

> [!CAUTION]
> Núverandi sérstilling á síðunni verður hreinsuð. Síðan mun fara aftur í upprunalegt útlit og þú verður að byrja frá grunni.  

## <a name="blocked-from-personalizing" />Lokað fyrir sérstillingar

Ef táknið ![Sérstilling útilokuð](media/personalization-blocked-icon.png "Sérstilling útilokuð") er á borðanum **Sérstilling** er búið að útiloka þig frá því að sérstilla síðuna.

<!-- Only text is translated, so removing this image for non-English UX reasons.  ![Personalize blocked.](media/personalization-blocked.png "Personalize lock") -->

Ástæðan er að Mitt hlutverk eða hlutverk sem er sem stendur tengt við notandareikninginn þinn breytir þessari síðu sérstaklega fyrir hlutverkið þitt. Hafðu samband við stjórnanda til að fá aðstoð. Að öðrum kosti skal reyna að skipta yfir í Mitt hlutverk sem inniheldur hlutverkaleik fyrir þessa síðu. Frekari upplýsingar eru í [Breyta grundvallarstillingum](ui-change-basic-settings.md).

## <a name="see-also" />Sjá einnig

[Sérstilling verksvæðis](ui-personalization-user.md)  
[Sérsníða síður fyrir forstillingar](ui-personalization-manage.md)  
[Grunnstillingum breytt](ui-change-basic-settings.md)  
[Breyta því hvaða eiginleikar eru sýndir](ui-experiences.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
