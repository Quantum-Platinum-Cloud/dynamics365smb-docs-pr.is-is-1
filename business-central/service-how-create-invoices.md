---
title: Stofna reikninga eða kreditreikninga fyrir þjónustu
description: Kynntu þér hvernig þú getur á einfaldan hátt notað Business Central til að búa til kreditreikning fyrir þjónustu þína.
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: bholtorf
---
# <a name="create-service-invoices-or-credit-memos" />Stofna Þjónustureikninga eða kreditreikninga
Auðveld reikningsfærsla þjónustupantana er lykileiginleiki [!INCLUDE[prod_short](includes/prod_short.md)]. Hægt er að setja [!INCLUDE[prod_short](includes/prod_short.md)] kerfið upp þannig að þjónustutæknimaður á vettvangi geti stofnað reikning fyrir þjónustu sem ekki er tengd samningi eða pöntun. Einnig er hægt að setja upp [!INCLUDE[prod_short](includes/prod_short.md)] til að reikningsfæra þjónustusamninga reglulega. Reikningstímabil samnings ræður tíðni reikningsfærslu.

## <a name="to-invoice-several-service-contracts" />Að reikningsfæra nokkra þjónustusamninga

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Stofna þjónustusamningsreikninga** og velja síðan viðkomandi tengil.  
2. Færa skal inn þær afmarkanir sem á að nota.  
3. Í reitnum **Bókunardags.** er færð inn dagsetningin sem á að nota sem bókunardagsetningu á þjónustureikningum.  
4. Í reitnum **Reikningsfæra til dags.** er færð inn dagsetningin sem á að reikningsfæra samninga til. Í keyrslunni verða samningar með næstu dags. reiknings að þessari dagsetningu.  
5. Í reitnum **Aðgerð** er valið að **Stofna reikninga**.  
6. Smellt er á **Í lagi** til að stofna þjónustureikningana.  
  
Einnig er hægt að reikningsfæra þjónustusamning beint af síðunni **Þjónustusamningur** ef næsta reikningsdags. samningsins er á undan vinnudagsetningunni.

## <a name="to-invoice-a-service-contract-from-the-service-contract-page" />Til að reikningsfæra þjónustusamning úr síðunni Þjónustusamningur
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustusamningar** og velja síðan viðkomandi tengil.  
2. Velja skal þjónustusamninginn sem á að reikningsfæra og opna samningsspjaldið.  
3. Veldu aðgerðina **Stofna þjónustureikning**. 
4. Smellt er á **Já** til að stofna þjónustureikningana.  
  
  > [!NOTE]  
  > Ekki er hægt að stofna þjónustureikninga fyrir þjónustusamning þegar gildið í reitnum **Breyta stöðu** er **Opið**.  

## <a name="to-post-an-invoice-from-a-service-order" />Bókun reikninga úr þjónustupöntunum
Eftirfarandi aðferð lýsir hvernig á að skilgreina þann þátt þjónustunnar sem verður skrifaður á reikning viðskiptamanns.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustupantanir** og svo velja viðeigandi tengil.  
2. Velja skal þjónustupöntunina sem á að reikningsfæra og opna pöntunarspjaldið.  
3. Veljið aðgerðina **Þjónustulínur**.  
4. Finndu færslurnar sem þörf er á og tilgreindu magnið sem á að skrifa á reikning viðskiptamanns í reitnum **Magn til reikningsf.**   
  
   > [!NOTE]  
   > Hægt er að reikningsfæra á viðskiptamann fyrir skráða þjónustu að hluta til eða til fulls. Ef valið er að reikningsfæra til fulls verður gildið í reitnum  **Magn til reikningsf.** að vera jafnt og gildið í reitnum  **Magn**. Hægt er að bóka reikning til fulls með afhendingu til fulls og hægt er að bóka reikning til fulls fyrir afhendingu til fulls sem þegar er búið að bóka en hefur hvorki verið reikningsfærð né notuð áður.  
   >  
   > Ef reikningur að hluta er bókaður eru tvær leiðir til þess að tilgreina magnið sem á að reikningsfæra. Ef þjónustan er bókuð með valkostinum **Afhenda og reikningsfæra** verður gildið í reitnum **Magn til reikningsf.** að vera jafnt og gildið í reitnum **Magn til afhendingar**. Ef ætlunin er að reikningsfæra bókaða afhendingu má magn til reikningsfærslu ekki vera meira en gildið í reitnum **Afhent magn**.  
  
5. Veldu **Bóka**, og svo annað hvort **Reikning** eða **Afhenda og reikningsfæra**. Til að fá nánari upplýsingar um valkosti sjá [Bókun í þjónustukerfi](service-service-posting.md).  
  
 Þjónustulínan sem valin hefur verið er bókuð. Hægt er að bóka margar þjónustulínur í einu með því að velja þær allar og velja **Bóka**. Ef það er gert þarf að tryggja að allar nauðsynlegar upplýsingar hafi verið færðar inn í línurnar sem á að bóka.  
  
 Þegar pöntun er bókuð með valkostinum **Reikningur** er bókaður þjónustureikningur stofnaður ásamt tilheyrandi fjárhagsfærslum og viðkomandi reitir í þjónustulínum pöntunarinnar uppfærðir. Þar að auki eru bókuð afhendingarfylgiskjöl uppfærð með magninu sem búið er að reikningsfæra. Ef bókunarmöguleikinn **Afhenda og reikningsfæra** er jafnframt stofnuð bókuð afhending.

## <a name="to-create-a-service-invoice-manually" />Þjónustureikningar búnir til handvirkt
Ef þjónustupöntun er bókuð með valkostinum **Reikningur** eða **Afhenda og reikningsfæra** býr forritið sjálfkrafa til bókaða reikningsfærslu. Eigi að síður gæti þurft að gefa út reikning sem hvorki er tengdur þjónustusamningi né þjónustupöntun. Þessi aðgerð útskýrir hvernig gefa á út reikning á sama tíma og viðskiptamaðurinn fær þjónustuna.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustureikningar** og velja síðan viðkomandi tengil.  
2. Nýr þjónustureikningur er stofnaður.  
3. Fylla þarf út reitinn **Nr.**. .  
  
    > [!NOTE]  
    >  Ef settar hafa verið upp númeraraðir fyrir þjónustureikninga á  **síðunni Þjónustukerfisgrunnur**  er hægt að velja  <kbd>Enter</kbd>  til að velja næsta tiltæka reikningsnúmer í þjónustu.  
  
4. Í **Númer viðskiptamanns** reitinn er fært inn númer viðskiptamanns. Veljið viðeigandi viðskiptamann af listanum.  
  
    Fyllt er í viðskiptavinareiti með upplýsingum úr spjaldinu **Viðskiptavinur**.  
  
5. Dagsetning er færð inn í reitinn **Bókunardags.** Þessi dagsetning mun birtast á bókuðum færslum. Þessi dagsetning mun birtast á bókuðum færslum. Þessi reitur er fylltur út með gildandi vinnudagsetningu, en hægt er að breyta honum handvirkt.  
6. Fylla skal út reitinn **Dagsetning fylgiskjals**. Dagsetningin sem færð er inn mun birtast á prentaða reikningnum og verður notuð til þess að reikna út gjalddaga.  
7. Fylla inn í þjónustulínur reikningsins. Fylla inn í reitina **Tegund**, **Nr.** og **Magn** til þess að skrá vörur, magn og kostnað sem notað hefur verið í þjónustu. 

## <a name="to-create-an-invoice-that-combines-posted-shipment-lines-from-one-or-more-service-orders" />Til að stofna reikning sem sameinar bókaðar sendingarlínur úr einni eða fleiri þjónustupöntunum
Ef til vill þarf að stofna þjónustureikning fyrir þjónustu sem þegar hefur verið afhent, annað hvort úr einni eða fleiri þjónustupöntunum, en ekki verið reikningsfærð ennþá eða notuð. Hægt er að fylla reikningslínurnar út sjálfkrafa ásamt völdum bókuðum afhendingarlínum fyrir tilgreindan viðskiptamann.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustureikningar** og velja síðan viðkomandi tengil.  
2. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)] 
3. Stofna skal reikningslínur fyrir afhenta þjónustu sem ekki er búið að reikningsfæra. Að öðrum kosti geturðu notað **Sækja afhendingarlínur** aðgerðina til að bæta bókuðum afhendingarlínum við reikninginn.  
4. Bóka skal þjónustureikninginn.  
  
 Bókaði þjónustureikningurinn og samsvarandi fjárhagsfærsla eru stofnuð. Áður bókuð afhendingarfylgiskjöl eru uppfærð með reikningsfærðu magni og viðeigandi magni í þjónustulínur upphafspöntunar/pantana.  

## <a name="to-create-a-service-credit-memo" />Þjónustukreditreikningar búnir til:
Þjónustukreditreikningur er yfirleitt notaður þegar viðskiptamaður skilar vöru, en hann er einnig hægt að nota til þess veita viðskiptamanni söluuppbót eða leiðrétta rangan reikning.  

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Þjónustukreditreikningar** og velja síðan viðkomandi tengil.  
2. Fyllið út reitina í línunni eins og þörf er á. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]
3. Reitirnir **Bókunardagsetning** og **Dagsetning fylgiskjals** sýna vinnudagsetninguna. Hægt er að breyta því ef þörf er á.    
4. Í kreditreikningslínurnar eru færðar upplýsingar um vörurnar sem hefur verið skilað eða hafa verið fjarlægðar, eða söluuppbót sem á að gefa viðskiptamanni.  

## <a name="see-also" />Sjá einnig
[Bóka þjónustureikninga](service-how-to-post-service-orders.md)  
[Þjónustustýring sett upp](service-setup-service.md)  
[Bókun þjónustu](service-service-posting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
