---
title: Hönnun lýsingar-framboð í vöruhúsi
description: Fræðast um mismunandi þætti sem hafa áhrif á vöruframboð í vöruhúsinu.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: conceptual
ms.date: 02/22/2023
ms.custom: bap-template
---
# <a name="design-details-availability-in-the-warehouse" />Hönnunarupplýsingar: Framboð á lager

Leggðu ofan á vöruframboð til að tryggja að pantanir á útleið flæði á skilvirkan hátt og að afhendingartímar þínir séu ákjósanlegir.  

Til ráðstöfunar geta verið mismunandi, allt eftir nokkrum þáttum. Fr dæmi:

* Úthlutanir á hólstigi þegar vöruhúsaaðgerðir eins og tínslur og hreyfingar gerast.
* Þegar takmarkanir á birgðafrátekningu eru settar saman til samræmis við það.

Áður en magni er úthlutað á tínslur fyrir streymi  [!INCLUDE [prod_short](includes/prod_short.md)]  á útleið sannprófar að öll skilyrði séu uppfyllt.

Þegar skilyrði eru ekki uppfyllt eru villuskilaboð sýnd. Eitt dæmigert boð er hið almenna "ekkert að höndla." skilaboð. Hægt er að sýna boðin af mörgum mismunandi ástæðum á útleið og á innleið þar sem fylgiskjalslína inniheldur  **reitinn Magn til afgreiðslu** .

## <a name="bin-content-and-reservations" />Innihald og frátekningar hólfs

Vörumagn er bæði til vöruhúsafærslur og sem birgðafærslur í birgðum. Þessar tvennskonar færslur innihalda mismunandi upplýsingar um hvaðan vörur eru og hvort þær séu tiltækar. Vöruhúsafærslur skilgreina framboð vöru eftir hólfi og hólfagerð, sem kallast innihald hólfs. Birgðafærslur skilgreina ráðstöfunarmagn vöru með frátekningu á skjölum á útleið.  

[!INCLUDE [prod_short](includes/prod_short.md)] reiknar út magnið sem er tiltækt til tínslu þegar innihald hólfs er leitt með frátekningum.  

## <a name="quantity-available-to-pick" />Tiltækt magn til tínslu

[!INCLUDE [prod_short](includes/prod_short.md)] tekur frá vörur fyrir sölupantanir sem bíða afhendingar svo að þær séu ekki teknar til annarra sölupantana sem senda fyrr. [!INCLUDE [prod_short](includes/prod_short.md)] dregur úr magni þeirra vara sem þegar er unnið með, sem hér segir:

* Magn sem er frátekið fyrir önnur skjöl á útleið.
* Magn á fyrirliggjandi tínsluskjölum.
* Magn tekið til en ekki enn afhent eða notað.  

Niðurstaðan er reiknuð út breytilegt og birt í  **reitnum Magn til tínslu**  á  **síðunni tínsluvinnublað** . Gildið er einnig reiknað út þegar notendur stofna tiltektir í vöruhúsi beint fyrir skjöl á útleið. Eftirfarandi eru dæmi um útleiðarskjöl:

* Sölupantanir
* Framleiðslugeyslu
* Millifærslur á útleið

Útkoman er tiltæk í þessum skjölum í reitunum magn eins og  **í reitnum Magn til afgreiðslu** .  

> [!NOTE]  
> Til að forgangsraða frátekningum, er magnið sem á að taka frá dregið frá því magni sem tiltækt er til tínslu. Til dæmis, ef magnið sem er tiltækt í tínsluhólfum er 5 einingar en 100 einingar eru í frágangshólfum þegar fleiri en 5 einingar eru fráleitar í annarri pöntun birtast villuskilaboð þar sem viðbótarmagnið verður að vera tiltækt í tínsluhólfum.  

### <a name="calculating-the-quantity-available-to-pick" />Magnið sem er tiltækt til tínslu er reiknað

[!INCLUDE [prod_short](includes/prod_short.md)] reiknar magnið sem er tiltækt til að velja á eftirfarandi hátt:  

magn tiltækt í tínslu = magn í tínsluhólfum - magn í tínslu og hreyfingar – (frátekið magn í tínsluhólfum + frátekið magn í tínslu og hreyfingu)  

Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.  

![Tiltækt í tínslu, með skörun í frátekningu.](media/design_details_warehouse_management_availability_2.png "Tiltækt í tínslu, með pöntunarskörun")  

## <a name="quantity-available-to-reserve" />Tiltækt magn til frátekingar

Þar sem hugtökin innihald hólfs og frátekt eru tiltæk er magn varanna sem eiga að taka frá frátekið að vera samræmt úthlutun á vöruhússkjölum á útleið.  

Hægt er að taka frá allar birgðavörur, nema vörur sem Úrvinnsla á útleið hefur ræst. Magnið sem er tiltækt til frátekingar er skilgreint sem magnið á öllum skjölum og hólfstegundum. Eftirfarandi magn á útleið eru undantekningar:  

* Magn í óskráðum tínsluskjölum  
* Magn í afhendingarhólfum  
* Magn í hólfkótum til framleiðslu  
* Magn í hólfkóta opins vinnslusalar  
* Magn í hólfum til samsetningar  
* Magn í leiðréttingarhólfum  

Niðurstöðurnar eru birtar í reitnum **Tiltækt heildarmagn** á síðunni **Frátekning**.  

Í frátekningarlínu er magnið sem ekki er hægt að taka frá þar sem því er úthlutað í vöruhúsinu birt í  **reitnum Magn úthlutað í vöruhúsi**  á  **frátekningarsíðunni** .  

### <a name="calculating-the-quantity-available-to-reserve" />Reiknað út tiltækt magn til frátekingar

[!INCLUDE [prod_short](includes/prod_short.md)] reiknar magnið sem er tiltækt til að taka frá sem hér segir:  

magn tiltækt í frátekningu = heildarmagn í birgðum - magn í tínslu og hreyfingu fyrir upprunaskjöl - frátekið magn - magn í hólfum á útleið  

Eftirfarandi skýringarmynd sýnir mismunandi þætti í útreikningi.  

![Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi.](media/design_details_warehouse_management_availability_3.png "Tiltækt í frátekningu, fyrir úthlutanir í vöruhúsi")  

## <a name="see-also" />Sjá einnig

[Yfirlit yfir](design-details-warehouse-management.md)
[vöruhúsastjórnun Skoða framboð á vörum](inventory-how-availability-overview.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
