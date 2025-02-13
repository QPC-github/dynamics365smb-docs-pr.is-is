---
title: Stjórna notendastillingum og kjörstillingum sem stjórnandi
description: Stjórna notendastillingum og kjörstillingum í Dynamics 365 Business Central.
author: sorenfriisalexandersen
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.reviewer: edupont
ms.search.keywords: 'user settings, preferences, language, region, time zone, regional settings'
ms.search.form: '9204,'
ms.date: 04/01/2021
ms.author: soalex
---
# <a name="manage-user-settings-and-preferences" />Stjórna notendastillingum og kjörstillingum

Sem stjórnandi getur þú skilgreint notandastillingar í [!INCLUDE[prod_short](includes/prod_short.md)], svipað því og einstakir notendur geta stjórnað eigin kjörstillingum á síðunni **Mínar stillingar**.  

Fáið yfirlit yfir alla notendur í listanum **Notendur** og breytið einstaka stillingum með því að velja aðgerðina **Notandastillingar** fyrir notandann sem á við.

> [!TIP]
> Listinn **Notandastillingar** sýnir núverandi stillingar fyrir hvern notanda. Til að skoða eða breyta einstökum notendum skal velja aðgerðina **Skoða** eða **Breyta**.

Síðan **Spjald notandastillinga** er svipuð og síðan **Mínar stillingar** sem hver notandi hefur aðgang að og er hún öflugt verkfæri fyrir stjórnendur til að stilla sjálfgefnar stillingar og hreinsa sérstilltar síður sem dæmi.  

## <a name="types-of-user-settings" />Gerðir notendastillinga

*Notandastillingar* eru ekki þær sömu og *Notandauppsetning*, sem er um notandann sem eining og aðgangur notanda í kerfinu. Notandastillingar hafa ennfremur ekkert að gera með sérstillingar notanda, t.d. minniháttar breytingum á notandaviðmóti. Notendastillingar ákvarða forskilgreindar  stillingar fyrir hvern notanda á þann ólíka hátt sem forritið birtist notandanum. Eftirfarandi málsgrein sýnir fimm gerðir notendastillinga og kjörstillingar sem einstakur notandi getur stillt eða stjórnandi stillir miðlægt:

* **Fyrirtæki**  

  Þessi stilling ákvarðar fyrirtækið sem er skráð inn í næstu innskráningu. Notandi getur haft aðgang að mörgum fyrirtækjum og getur verið virkur í nokkrum fyrirtækjum.

* **Hlutverk**  

  Hlutverkið eð forstillingin lýsir hlutverki notanda í fyrirtækinu, t.d. *Sölustjóri*, *Bókari* eða *Innkaupafulltrúi*. Forstillingin ákvarðar síðan hlutverkamiðstöð notandans, heimasíðuna sem notendur sjá þegar hann skráir sig inn. Forstillingin hefur ekki áhrif á aðgangsheimild að virkni í [!INCLUDE[prod_short](includes/prod_short.md)].  

* **Tungumál**  

  Skilgreinir forritstungumál sem [!INCLUDE[prod_short](includes/prod_short.md)] birtir texta, textar og villuskilaboð á. Ef [!INCLUDE[prod_short](includes/prod_short.md)] notendur eru samstilltir frá Microsoft 365 eru tungumálastillingar frá Microsoft 365 notaðar, að því gefnu að notandinn vilji nota sömu stillingar í Office-vörum og [!INCLUDE[prod_short](includes/prod_short.md)]. Stjórnandinn getur breytt sjálfgefinni stillingu og hver notandi getur valið á milli tiltækra tungumála á síðunni Mínar stillingar. En þær verða endurstilltar á gildið frá Microsoft 365 þegar næsta samstilling er framkvæmd.

  Ef tungumálastillingin úr Microsoft 365 samsvarar studdu tungumáli í [!INCLUDE[prod_short](includes/prod_short.md)] verður slíkt tungumál valið fyrir notandann.  

  > [!NOTE]
  > Hugsanlega þarf að setja upp tungumálaforrit fyrir [!INCLUDE[prod_short](includes/prod_short.md)] til að birta tungumálið á réttan hátt. Þar af leiðandi er það góð venja að setja upp nauðsynleg tungumálaforrit áður en einhver notandi skráir sig inn í fyrsta skipti þannig að þeir fái góða upplifun frá byrjun. Frekari upplýsingar er að finna í listanum yfir [studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations).  
  
* **Svæði**  

  Skilgreinir hvernig dagsetningar og tölustafir birtast í [!INCLUDE[prod_short](includes/prod_short.md)] -biðlaranum, svo sem hvort nota eigi evrópskar eða bandarískar dagsetningarsnið eða hvernig á að birta tugabrotin og þúsund skiltákn í upphæðum. Ef [!INCLUDE[prod_short](includes/prod_short.md)] notendur eru samstilltir frá Microsoft 365 eru svæðisstillingarnar frá Microsoft 365 notaðar, að því gefnu að notandinn vill nota sömu stillingar í Office-vörum og [!INCLUDE[prod_short](includes/prod_short.md)]. Stjórnandi eða notandi getur breytt þessum stillingum handvirkt í [!INCLUDE[prod_short](includes/prod_short.md)], en þær verða endurstilltar á gildið frá Microsoft 365 þegar næsta samstilling er framkvæmd.

* **Tímabelti**  

  Skilgreinir tímabeltið þar sem notandinn er staðsettur. Sem stendur er þetta ekki samstillt af Microsoft 365 og verður að stilla handvirkt.  

* **Kennsluábendingar**

  [!INCLUDE [ua-teachingtips](includes/ua-teachingtips.md)] Sem stjórnandi geturðu slökkt á fróðlegum ábendingum fyrir alla notendur, t.d. ef þú ert að innleiða notendur sem eru nú þegar kunnugir [!INCLUDE [prod_short](includes/prod_short.md)].  

> [!NOTE]
> Ef samstilling Microsoft 365 -notanda er gerð á meðan notendur eru skráðir inn í [!INCLUDE[prod_short](includes/prod_short.md)] verða slíkir notendur að uppfæra vafrann eða skrá sig út og aftur inn í [!INCLUDE[prod_short](includes/prod_short.md)] til að sjá þeir geti séð annað tungumál sem er stillt með samstillingaraðgerðinni.

## <a name="overview-of-all-user-specific-changes" />Yfirlit yfir notandabundnar breytingar

Sem stjórnandi geturðu fengið yfirlit yfir einstaka breytingar á [!INCLUDE [prod_short](includes/prod_short.md)] sem hver notandi gæti hafa gert á ýmsum síðum í [!INCLUDE [prod_short](includes/prod_short.md)]. Þegar notendur gera breytingar á upplifun sinni í [!INCLUDE [prod_short](includes/prod_short.md)] munu þær koma fram í listanum **Sérstillingar notanda**. <!--Administrators can also set these settings for users before they log in the first time, so users do not have to do it themselves, providing them a better *getting started* experience.-->

<!-- >[!NOTE]
> User personalizations do not have anything to do with the *personal* lightweight changes a user can make to the user experience.-->

## <a name="to-review-or-delete-user-personalizations" />Að yfirfara eða eyða sérstillingum notanda

1. Veldu ![Leita að síðu eða skýrslu.](media/ui-search/search_small.png "Leit að síðu eða skýrslu tákn") táknið, farðu í **Sérsniðnar síður** og veldu svo viðeigandi tengil.
2. Þetta birtir lista yfir notendur og sérstilltar síður þeirra. Til að hreinsa sérstillingu notanda er smellt á viðeigandi línu eða valið **Stjórna** og síðan valið **Eyða**.

Þetta eyðir sérstillingum og upplifun notandans á viðkomandi síðu fer aftur í sjálfgefna stöðu.

## <a name="see-also" />Sjá einnig

[Undirbúðu þig fyrir að gera viðskipti](ui-get-ready-business.md)  
[Lönd/svæði í boði og studd tungumál](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations)  
[Breyta tungumáli og landsstaðli](about-locale-language.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
