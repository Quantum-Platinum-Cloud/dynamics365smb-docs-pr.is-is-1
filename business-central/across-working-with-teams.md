---
title: Deila Business Central Records í Microsoft Teams
description: Fá upplýsingar um notkun Business Central fyrir Microsoft Teams.
author: jswymer
ms.topic: how-to
ms.service: dynamics365-business-central
ms.reviewer: jswymer
ms.search.keywords: 'Teams, MS Teams, Microsoft Teams, Skype, Link, Microsoft 365, collaborate, collaboration, teamwork, share records'
ms.date: 16/18/2023
ms.author: jswymer
ms.custom: bap-template
---

# <a name="sharing-business-central-records-and-page-links-in-microsoft-teams" />Deila færslum Business Central og síðutenglum í Microsoft Teams

[!INCLUDE [online_only](includes/online_only.md)]

[!INCLUDE [prod_short](includes/prod_short.md)] býður upp á nokkrar leiðir til að deila gögnum úr Business Central beint í Microsoft Teams samtal:

<!-- 
## <a name="overview" />Overview
In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.
The [!INCLUDE [prod_short](includes/prod_short.md)] app lets you:
[!INCLUDE [prod_short](includes/prod_short.md)] offers an app that connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)], so you can quickly share details across team members and respond faster to inquiries. In this article, you'll learn how to use the app to share [!INCLUDE [prod_short](includes/prod_short.md)] records, like a customer, sales order, or invoice, with coworkers in a Teams conversation.

-->
- Með [!INCLUDE [prod_short](includes/prod_short.md)] forritið uppsett í Teams er hægt að hafa með gagnvirkt spjald af færslu Business Central í Teams-samtali.

<!--   Copy a link from any Business Central record, like a customer or sales order, then paste the link into a Teams conversation. The app connects Microsoft Teams to your business data in [!INCLUDE [prod_short](includes/prod_short.md)]. It then expands the link into a compact, interactive card that displays information about the record. Once in the conversation, you and coworkers can view more details about the record, edit data, and take action&mdash;without leaving Teams.

  [![Teams integration with Business Central.](media/teams-intro-v3.png)](media/teams-intro-v3.png#lightbox)-->

- Með eða án þess að [!INCLUDE [prod_short](includes/prod_short.md)] forritið er uppsett er hægt að deila tengli af síðunum í Business Central í samtali í Teams.

  <!-- ![!The Share menu displayed on a card.](media/teams-share-link.png "The Share menu displayed on a card.")-->

Eftirfarandi hlutar útskýra mismunandi leiðir í smáatriðum.

## <a name="include-and-view-a-business-central-card-in-a-teams-conversation" />Hafa með og skoða Business Central-spjald í samtali í Teams

Með forriti Business Central fyrir Teams er hægt að afrita tengli úr hvaða Business Central-færslu sem er, t.d. viðskiptavina- eða sölupöntun, og líma tengilinn í samtal í Teams. Forritið tengir Microsoft Teams við viðskiptagögnin í [!INCLUDE [prod_short](includes/prod_short.md)]\. Því næst er tengillinn stækkaður í gagnvirkt spjald sem birtir upplýsingar um færsluna. Þegar á samtalinu stendur getur þú og samstarfsfólk þitt skoðað frekari upplýsingar um færsluna, breytt gögnum og gripið til aðgerða &mdash; án þess að fara úr Teams.

[![Samþætting Teams við Business Central.](media/teams-intro-vBC20.png)](media/teams-intro-vBC20.png#lightbox)

### <a name="prerequisites" />Frumskilyrði

- Þú hefur aðgang að Microsoft Teams.
- Þú hefur sett upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið  í Teams. Frekari upplýsingar er að finna í [Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)

> [!NOTE]
> Allir þátttakendur í Teams-spjalli geta skoðað spjöld fyrir færslur Business Central sem þú sendir inn á spjallið. En til að skoða frekari upplýsingar um færslur með því að nota hnappana **Upplýsingar** eða **Sprettigluggi** á spjaldi, þurfa þeir að fá aðgang að [!INCLUDE [prod_short](includes/prod_short.md)]. Nánari upplýsingar er að finna í [Stjórnun Microsoft Teams samþættingar](admin-teams-integration.md#minimum-requirements-1).

### <a name="include-a-business-central-card-in-a-teams-conversation" />Hafa með Business Central-spjald í samtali í Teams

1. Skráðu þig inn í [!INCLUDE [prod_short](includes/prod_short.md)] með vafranum.
2. Opnið færsluna sem á að deila.

    Forritið er hannað til að sýna spjald fyrir næstum hvaða tegund af [!INCLUDE [prod_short](includes/prod_short.md)] síðu sem er. En það býður upp á bestu upplifunina þegar það er notað fyrir síður sem sýna eina færslu, t.d. vöru, viðskiptamann eða sölupöntun.
3. Afritaðu tengilinn á síðuna.

    Hægt er að afrita tengilinn á tvo vegu. Auðveldasta og ákjósanlegasta leiðin er að velja **Deila** ![Deilingartákn í Business Central](media/share-icon.png) > **Afrita tengil**. Hin leiðin er að afrita alla vefslóðina úr veffangastiku vafrans.

    [![Afritið vefslóð Business Central úr vafra.](media/teams-copy-link.png)](media/teams-copy-link.png#lightbox)
4. Farið í Teams og hefjið samtal sem getur verið spjall við einstakling, hóp eða teymisrás.
5. Límið tengilinn (slóðina) í skilaboðagluggann þar sem skrifuð eru skilaboð.

    ![Límið vefslóð Business Central í Teams.](media/teams-paste-url-v2.png)

    > [!TIP]
    > Ef þú færð skilaboð eins og: *Business Central vill sýna forskoðun á þessum tengli* þýðir það að þú ert ekki með Business Central-forritið fyrir Teams uppsett. Til að setja upp forritið skal velja **Sýna forskoðun** og fylgja leiðbeiningunum.

    > [!NOTE]
    > Allt frá því að þú ert Aðalútgáfa viðskipta, í fyrsta sinn sem tengill er límdur á samtal, getur verið að notandi sé beðinn um að skrá sig inn  [!INCLUDE [prod_short](includes/prod_short.md)]  og gefa samþykki fyrir því að App sæki gögn. Fylgdu leiðbeiningunum á skjánum. Þú munt aðeins þurfa að gera þetta skref einu sinni.
6. Bíðið augnablik á meðan spjald er búið til í skilaboðaglugganum.
7. Þegar spjaldið birtist skal leita vel og vandlega í innihald þess eftir viðkvæmum upplýsingum áður en skilaboðin eru send. Þetta skref er mikilvægt vegna þess að þegar skilaboðin eru send geta allir í samtalinu séð spjaldið.
8. Ef spjaldið lítur vel út skal velja **Senda** til að senda það í samtalið.

    > [!TIP]
    > Eftir að kortið birtist og áður en **Senda** er valið er hægt að eyða límdri vefslóð ef þú vilt.
9. Til að fá frekari upplýsingar eða gera breytingar á færslunni sem birtist í spjaldinu skal velja **Upplýsingar**. Nánari upplýsingar er að finna í næsta hluta.

### <a name="view-card-details" />Skoða upplýsingar spjalds

Þegar búið er að senda spjald á samtal, geta allir þátttakendur með [viðeigandi heimildir](admin-teams-integration.md#permissions) valið **Upplýsingar** til að opna glugga sem sýnir frekari upplýsingar um færsluna&mdash;og hugsanlega geta gert breytingar á henni. Það skiptir ekki máli hvort það sért þú sem sendir spjaldið eða sá sem fær spjaldið. Eiginleikinn **Upplýsingar** er sérstaklega gagnlegur viðtakendum af því að hann veitir þeim samanteknar, hnitmiðaðar upplýsingar um færsluna á fljótlegan hátt.

Upplýsingaglugginn er svipaður því sem þú myndir sjá í [!INCLUDE [prod_short](includes/prod_short.md)] en hann einblínir á síðuna eða færsluna sem spjaldið er um. Þegar skoðun er lokið og breytingar hafa verið gerðar skal loka glugganum til að fara aftur í samtalið í Teams.

Hér eru nokkur atriði sem vert er að hafa í huga þegar unnið er með upplýsingar spjalds:

- Til að opna upplýsingar spjalds verða notendur að vera með heimild á síðunni og gögnum þess í [!INCLUDE [prod_short](includes/prod_short.md)]\.
- Spjöld í Teams-spjalli uppfærast ekki sjálfkrafa þegar gerðar eru breytingar. Allar breytingar sem eru vistaðar í færslu í upplýsingaglugganum eru vistaðar í [!INCLUDE [prod_short](includes/prod_short.md)]\. En spjaldið í Teams sýnir ekki breytingarnar í samtalinu fyrr en tengillinn er límdur inn aftur.

Frekari upplýsingar um hvernig nota á spjöld og upplýsingar spjalds er að finna í [Teams - Algengar spurningar](teams-faq.md).

## <a name="a-nameshare-linkashare-a-link-to-page-from-business-central-to-teams" /><a name="share-link"></a>Deila tengli á síðu úr Business Central í Teams

Beint af flestum innheimtusíðum eins og **Vörusíðum** og upplýsingasíðum eins og **Birgðaspjaldi** er hægt að senda tengil á síðuna til tiltekinna viðtakenda í samtali í Teams. Til dæmis er hægt að deila tengli á síað yfirlit yfir færslurnar þínar. Viðtakendur geta þá valið tengilinn til að opna síðuna í [!INCLUDE [prod_short](includes/prod_short.md)]\.

[![!Deilingarvalmynd sýnd í spjaldi.](media/teams-share-link-v2.png "Deilingarvalmyndin sýnd á spjaldi.")](media/teams-share-link-v2.png#lightbox)

### <a name="prerequisites" />Frumskilyrði

- Þú hefur aðgang að Microsoft Teams.
- (Valkvæmt) Þú hefur sett upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið  í Teams. 

  Með forritið uppsett munu skilaboð sem þú sendir með tenglinum einnig innihalda samandregið spjald fyrir síðuna. Frekari upplýsingar um uppsetningu forritsins er að finna í [Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md).

### <a name="share-a-link" />Deila tengli

1. Í [!INCLUDE [prod_short](includes/prod_short.md)]\, skal opna síðuna sem á að deila.
2. Efst á síðunni skal velja ![!Deila á aðrar forritsaðgerðir á síðum.](media/share-icon.png) síðan **Deila með Teams**.
3. Ef beðið er um innskráningu í Teams með notandanafninu þínu og lykilorði.
4. Á síðunni **Deila með Teams** skal slá inn heiti einstaklings, hóps eða rásar sem á að senda skilaboðin til.
5. Skilaboðaglugginn mun innihalda tengil á síðuna. Ef [!INCLUDE [prod_short](includes/prod_short.md)] forritið fyrir Team er uppsett mun spjald fyrir tengdu færsluna eða síðuna einnig birtast í upplýsingareitnum.

   Bættu við frekari upplýsingum ef þú vilt og veldu svo **Deila**.
6. Tenglinum hefur nú verið deilt. Ef þú vilt fara í samtalið skaltu velja **Fara í Teams**.

## <a name="see-also" />Sjá einnig .

[Business Central og Microsoft Teams samþættingaryfirlit](across-teams-overview.md)  
[Setja upp [!INCLUDE [prod_short](includes/prod_short.md)]-forritið fyrir Microsoft Teams](across-install-app-for-teams.md)  
[Teams - Algengar spurningar](teams-faq.md)  
[Leitar að viðskiptavinum, lánardrottnum og öðrum tengiliðum úr Microsoft Teams](across-search-contacts-teams.md)  
[Breyta fyrirtæki og aðrar stillingar í Teams](across-teams-settings.md)  
[Úrræðaleit Teams](admin-teams-troubleshooting.md)  
[Þróun fyrir samþættingu Teams](/dynamics365/business-central/dev-itpro/developer/devenv-develop-for-teams)  

## <a name="includeprodshortincludesfreetrialmdmd" />[!INCLUDE[prod_short](includes/free_trial_md.md)]

[!INCLUDE[footer-include](includes/footer-banner.md)]
