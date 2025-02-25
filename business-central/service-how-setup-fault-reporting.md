---
title: Uppsetning bilanatilkynninga í þjónustukerfi
description: Bilanatilkynningar gera þér kleift að setja fram staðlaða fyrir upplýsingar um bilanaskráningu fyrir þjónustuvörur með bilanakóðum og fleira.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/23/2021
ms.author: edupont
---

# <a name="set-up-fault-reporting" />Setja upp bilanatilkynningar
Bilanatilkynningar gera þér kleift að setja fram staðla tengda tilkynningum bilanaupplýsinga fyrir þjónustuvörur. Þú getur t.d. tilgreint hvert vandamálið er, einkennin sem þú sérð, ástæðu vandamálsins og hvernig skal leysa það.  

Bilanakóðar lýsa dæmigerðum bilunum í þjónustuvöru eða aðgerðir á þjónustuvöru. Eftir því hvernig bilanatilkynningum er háttað hjá fyrirtækinu kann einnig að vera nauðsynlegt að skrá bilanasvæðiskóta og einkennakóta þegar bilanakóti er skráður. Bilanasvæði lýsa svæðum með bilun í þjónustuvöru. Bilanaástæðukóta lýsa ástæðum fyrir bilun í þjónustuvöru og, ef með þarf, hvort skal útiloka ábyrgð og samningsafslátt. Til dæmis kemur til greina að útiloka ábyrgð og samningsafslátt ef viðskiptamaður var á einhvern hátt ábyrgur fyrir biluninni í þjónustuvörunni. Þú úthlutar bilanaástæðukóðar til þjónustupantana. Frekari upplýsingar eru í [Vinna með þjónustuverkhluta](service-how-to-work-on-service-tasks.md).  

## <a name="to-specify-the-overall-level-of-fault-reporting" />Tilgreina heildarstig bilanatilkynninga
1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning þjónustu** og svo velja viðeigandi tengil.
2. Í reitnum **Stig bilanatilkynninga** skal velja einn af valmöguleikunum í eftirfarandi töflu.  

    |**Bilanastig**|**Lýsing**|  
    |------------|-------------|  
    |Engin | Engir tilkynningakótar eru notaðir.|  
    |Bilun | Kótar eru gefnir upp á töflunni **Bilunarkótar**. Þessir kótar auðkenna bilanir í þjónustuvörum eða aðgerðir sem framkvæma á fyrir þjónustuvörur. Hægt er að klasa tengda kóða saman í flokkanir **bilanasvæðiskóða**.|  
    |Bilun + Einkenni | Samsetning kóta er gefin upp í töflunum **Bilunarkótar** og **Einkennakótar**. Dæmigerðir einkennakótar eru vísar sem viðskiptamaður gæti notað til að lýsa vandamáli, eins og hávaða eða gæðum.|  
    |Bilun + Einkenni + Svæði | Kóðarnir Bilun, Einkenni og Bilanasvæði eru notaðir til að innleiða alþjóðlega viðgerðarkóðunarkerfið (IRIS).|  

Til að ljúka uppsetningu bilanatilkynninga er einnig hægt að tilgreina hvaða viðgerðir eða úrlausnir tengjast bilun eða galla. Þú setur það upp á síðunni **Vensl bilana-/úrslausnarkóða** þar sem þú setur upp samsetningar kóða fyrir þjónustuvöruflokk þeirrar þjónustuvörunnar þar sem glugginn var opnaður í og fjöldi tilvika hvers og eins.

## <a name="to-create-fault-and-resolution-code-relationships" />Hvernig á að stofna Venslum bilana- og úrlausnarkóta
<!--this needs to go in a working with topic-->
 Hægt er að skoða algengustu viðgerðir á tilteknum vörubilunum þegar unnið er við þjónustu á vörunni ef búið er að skipuleggja upplýsingar um vensl bilana- og úrlausnarkóða. Nota skal keyrsluna **Setja inn tengsl bilana/úrlausnakóða** til að finna allar samsetningar bilana- og úrlausnarkóða í bókuðum þjónustupöntunum og skrá þær á síðuna **Tengsl bilunar/úrlausnarkóða**.

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Setja inn tengsl bilana/úrlausnakóða** og velja síðan viðkomandi tengil.  
2. Færðu inn dagsetningar til að skilgreina tímabilið sem keyrslan á að ná til.  
3. Veljið gátreitinn **Tengsl byggð á þjónustuvöruflokki** til að flokka tengslin eftir þjónustuvöruflokkum.  
4. Ef óskað er eftir því að varðveittar séu færslur sem þegar er búið að handfæra á síðunni **Tengsl bilana/úrlausnarkóða** skal velja gátreitinn **Varðveita handfærðar færslur**.  

## <a name="see-also" />Sjá einnig
[Þjónustustýring sett upp](service-setup-service.md)  
[Þjónustukerfi](service-service.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
