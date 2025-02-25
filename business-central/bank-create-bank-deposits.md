---
title: Búa til innborganir í banka
description: Þú getur lagt inn til að halda færsluskrá sem inniheldur upplýsingar sem hægt er að nota á útistandandi reikninga og kreditreikninga.
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '10140, 10141, 10143, 10144, 10146, 10147, 10148, 36646'
ms.date: 04/01/2021
ms.author: bholtorf
---
# <a name="create-bank-deposits" />Búa til innborganir í banka
> [!NOTE]
> Hæfileikinn til að búa til innistæður í banka er nýtt í Business Central 2022 útgáfu 1 fyrir mikið af landsútgáfum Ef þú varst að nota Business Central í Bandaríkjunum, Kanada eða Mexíkó fyrir þá útgáfu gætirðu verið að nota fyrri eiginleikana. Þú getur haldið áfram en nýju eiginleikarnir koma í stað þeirra gömlu í nýrri útgáfu. Til að byrja að nota nýju eiginleikana sem lýst er í þessari grein getur stjórnandi farið á síðuna **„Eiginleikastjórnun“** og kveikt **á „Eiginleikauppfærsla“: Stöðluð bankaafstemming og staðlaðar innborganir**.  

Notaðu síðu **innborganir í banka** til að skrá innborganir sem eitt skjal sem færir eina eða fleiri færslur á bankareikning. Venjulega eru bankainnstæður notaðar til að skrá innistæður í reiðufé. Síðan innborganir í banka er aðgengileg á valmyndinni **Reiðufjárstjórnun** í Hlutverkamiðstöð viðskiptastjórnanda og öðrum Hlutverkamiðstöðvum sem fjalla um reiðufjárstjórnun.

Fjárhæðir á bankainnstæðum geta komið úr ýmsum áttum:

* Sala, með því að nota fjárhagsreikning fyrir tekjur.
* Greiðslum viðskiptavina.
* Endurgreiðsla með reiðufé frá lánardrottnum eða greiðslur með reiðufé til þeirra. 

Innborgunarlínur banka innihalda upplýsingar um einstakar innstæður, svo sem ávísanir frá viðskiptavinum. Heildarupphæðin á línunum verður að stemma við heildarupphæð innborgunarinnar.

Eftir að búið er að fylla inn upplýsingar og línur innborgunar verður að bóka þær. Bókun mun uppfæra viðeigandi fjárhagi. Þar á meðal er fjárhagur og banka-, viðskiptavina- og lánardrottnabækur. Bókaðar innborganir eru geymdar til síðari nota á síðunni **Bókaðar innborganir í banka**.

Skýrslan **Innborganir í banka** sýnir innborganir viðskiptavina og lánardrottna með upphaflegri innborgunarupphæð, innborgunarfjárhæðinni sem er opin og upphæðinni sem er jöfnuð. Skýrslan sýnir einnig heildarfjárhæð bókaðrar innborgunar til að afstemma.

## <a name="before-you-start" />Verður að byrja fyrir
Þú þarft að setja upp nokkur atriði áður en þú getur notað innborganir í banka. Þú þarft að vera með númeraraðir og færslubókarsniðmát tilbúið. Þú ættir einnig að tilgreina hvort bóka eigi upphæðir innborgana í banka sem eingreiðslu. Þ.e. sem heildarupphæð allra upphæðanna á innlánalínunum. Annars er hver lína bókuð sem stök færsla. Með því að birta innborgun sem eina bankafærslu getur verið auðveldara að gera bankaafstemmingu.

### <a name="number-series-and-lump-sum-deposits" />Númeraraðir og innborganir eingreiðslu
Þú verður að setja upp númeraraðir fyrir innborganir í banka og tilgreina röðina svo í reitnum **Nr. innborgana í banka** á síðunni **Sölugrunnur**. Nánari upplýsingar sjá [Búa til Númeraröð](ui-create-number-series.md). 

Einnig á síðunni **Sölugrunnur**, ef þú vilt bóka innborganir sem eingreiðslur frekar en stakar línur, kveiktu þá á **Bóka innborganir í banka sem eingreiðslu**. Ef innborgun er bókuð sem eingreiðsla, sem býr til eina færslu í bankabók fyrir alla innborgunina, getur það auðveldað bankaafstemmingu.

### <a name="general-journal-templates-for-bank-deposits" />Sniðmát færslubóka fyrir innborganir í banka
Einnig þarf að búa til sniðmát færslubókar fyrir innborganir. Þú notar fjárhag til að bóka færslur í banka-, viðskiptavina-, lánardrottna, eignar- og fjárhagsreikninga. Sniðmát færslubókar hanna færslubókina þannig að hún henti tilgangi vinnunnar. Þ.e. reitir í sniðmáti færslubókar eru nákvæmlega þeir reitir sem þörf er fyrir. 

Innborganirnar verða inngreiðslur svo þú gætir viljað endurnýta númeraraðirnar fyrir inngreiðslubækur. Ef þú þarft að greina á milli innborgunar í banka og færslna í inngreiðslubók skaltu nota aðra númeraröð.

Einnig þarftu að búa til runuvinnslu fyrir sniðmátið. Til að búa til runuvinnslu, á síðunni **Sniðmát færslubókar**, skal velja aðgerðina **Runur**. Sjá [Nota sniðmát færslubóka og keyrslur](ui-work-general-journals.md#use-journal-templates-and-batches) fyrir frekari upplýsingar.

## <a name="dimensions-on-bank-deposit-lines" />Víddir innborgunarlína banka
Innborgunarlínur banka nota sjálfkrafa sjálfgefnar víddir sem tilgreindar eru í reitunum **Deildarkóði** og **Kóði viðskiptavinaflokks**. Þegar þú velur **viðskiptavin** eða **lánardrottin** í reitnum **Tegund reiknings** koma víddirnar sem eru tilgreindar fyrir viðskiptavininn eða lánardrottinn í staðinn fyrir sjálfgefnu víddirnar. Hægt er að breyta víddum á línunum, ef þarf.

> [!TIP]
> Víddir á línum er stilltur í samræmi við sjálfgefinn víddarforgang. Línuvíddum forgangsraðað yfir hausvíddir. Til að forðast árekstra er hægt að búa til reglur sem forgangsraða því hvenær nota á vídd eftir uppruna. Ef á að breyta því hvernig víddum er forgangsraðað er hægt að breyta röðun þeirra á síðunni **Sjálfgefinn víddarforgangur**. Frekari upplýsingar eru í [Að setja upp sjálfgefinn víddarforgang](finance-dimensions.md#to-set-up-default-dimension-priorities).

## <a name="create-a-bank-deposit" />Búa til innborgun í banka
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innborganir í banka** og velja síðan viðkomandi tengil.
2. Velja **Nýtt** til að opna síðuna **Innborgun í banka**. 
3. Veldu sniðmát færslubókar sem þú bjóst til fyrir innborganir í banka.  

    > [!NOTE]
    > Ef sniðmát færslubókar er með fleiri en eina runu verður þú beðin(n) um að velja eina slíka.

4. Í reitnum **Númer bankareiknings** er valinn sá bankareikningur sem leggja skal inn á.

    > [!TIP]
    > Þú getur gengið úr skugga um að þú sért að leggja inn á réttan reikning með því að nota aðgerðirnar **Reikningsspjald** og **Fjárhagsfærslur** til að fletta upp fjárhagsfærslum fyrir valinn bankareikning. Til dæmis til að sjá hvort svipaðar innborganir hafi verið gerðar á reikninginn.

5. Í reitinn **Heildarupphæð innborgunar** heildarupphæð innborgunar færð inn. Heildarupphæðin verður að vera samtala upphæðanna á öllum línunum.
6. Fyllið inn í eftirstandandi reiti eftir þörfum. [!INCLUDE [tooltip-inline-tip_md](../archive/SetupAndAdministration/includes/tooltip-inline-tip_md.md)]

    Dagsetningin í **Bókunardagsetning** og víddirnar í reitunum **Deildarkóði** og **Kóði viðskiptavinaflokks** verða settar í línurnar sem þú býrð til fyrir innborgunina í banka. Hægt er að breyta þeim ef óskað er. 

7. Það fer eftir því hvort þú vilt bóka innborgunina í banka sem eingreiðslu eða hverja línu fyrir sig á bankabókina hvort kveikt sé á **Bóka sem eingreiðslu** eða ekki. Sjálfgefin stilling er valin á sama hátt á síðunni **Sölugrunnur**.

    > [!NOTE]
    > Reiturinn **Gjaldmiðilskóði** sýnir gjaldmiðilinn sem er tilgreindur fyrir bankareikninginn sem þú valdir. Þú getur ekki valið annan gjaldmiðil.

8. Á flýtiflipanum **Línur** skal stofna nýja línu fyrir hverja greiðslu í reiðufé sem á að leggja inn.
9. Í reitnum **Tegund reiknings** er tilgreint hvaðan greiðslan er upprunnin. Fyrir innborganir í banka er tegundin yfirleitt **Viðskiptavinur** eða **Lánardrottinn**. 

    > [!NOTE]
    > Einnig er hægt að skrá greiðslu í reiðufé á lánardrottinn. Til að gera það velur þú **Lánardrottinn** og slærð síðan inn greiðsluupphæðina sem neikvætt númer í reitinn **Kreditupphæð** í línunni. 

10. Í reitnum **Númer fylgiskjals** er fært inn númer reikningsins þar sem kreditupphæðin er upprunnin. Þú getur notað fylgiskjalsnúmer fyrir hverja línu eða sama númer fyrir allar línur.

    > [!TIP]
    > Venjulega þarftu ekki að fylla út reitinn **Tegund fylgiskjals** fyrir fjárhagsfærslur. Ef þú ert til dæmis að leggja inn reiðufé af sölu dagsins geturðu skilið reitinn eftir auðan. Ef þú ert að leggja inn reiðufé af greiðslu viðskiptamanns velur þú **Greiðsla**.

11. Ef þú ert að leggja inn staðgreiðslu fyrir tiltekinn reikning viðskiptavinar velur þú aðgerðina **Jafna færslur** og slærð svo inn reikningsnúmerið í reitinn **Kenni jöfnunar**. 
12. Veldu aðgerðina **Bóka** ef alllt er til reiðu að bóka innborgunina í banka.

    > [!TIP]
    > Áður en þú bókar innborgunina getur þú notað aðgerðina **Prófunarskýrsla** til að fara yfir gögnin þín. Skýrslan mun sýna hvort einhver vandamál eins og gögn sem vantar, komi í veg fyrir bókun.  

## <a name="finding-posted-bank-deposits" />Leit að bókuðum innborgunum í banka
Á síðunni **Bókaðar innborganir í banka** eru fyrri innborganir fyrirtækisins skráðar. Í listanum er hægt að fara yfir athugasemdir og víddir sem voru tilgreindar fyrir innborganirnar. Þú getur opnað innborgunina í banka til að skoða nánari upplýsingar og kannað málið frekar. Til dæmis er hægt að velja aðgerðina Leita að færslum til að skoða bókaðar færslur í bankabókum. Í færslu bankabókar má finna samsvarandi bókaða fjárhagsfærslu.

Ef þú vilt fletta upp öllum fjárhagsfærslum í bókuðum innborgunarlínum skaltu fara á síðuna **Fjárhagsdagbók** og nota aðgerðina **Fjárhagur**. Þar er að finna allar fjárhagsfærslur, þar á meðal færslur fyrir viðskiptavini og lánardrottna.

## <a name="reversing-a-posted-bank-deposit" />Bakfærsla bókaðrar innborgunar í banka
Til að bakfæra bókaða innborgun ferðu á síðuna **Fjárhagsdagbækur** finnur dagbókina fyrir innborgunina og velur svo aðgerðina **Bakfæra dagbók**.

> [!NOTE]
> Aðeins er hægt að bakfæra dagbók sem inniheldur eina tegund færslu. Þ.e. dagbókin má aðeins innihalda færslur viðskiptavina eða færslur lánardrottna, en ekki bæði. Ef dagbók inniheldur hvort tveggja verður að bakfæra innborgunina handvirkt.      

## <a name="see-also" />Sjá einnig
[Fjármál](finance.md)  
[Uppsetning Fjármála](finance.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]



