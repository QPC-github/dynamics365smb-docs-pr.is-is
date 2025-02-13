---
title: Reikna dagsetningar pöntunarloforða
description: Pöntunarloforðsaðgerðin nýtist til að reikna fyrstu hugsanlegu dagsetningu fyrir sendingu eða afhendingu á vöru.
author: edupont04
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/29/2021
ms.author: edupont
---
# <a name="calculate-order-promising-dates" />Reikna dagsetningar pöntunarloforða

Fyrirtæki verður að geta upplýst viðskiptamenn sína um afhendingardagsetningar pöntunar. Síðan **Línur pöntunarloforðs** gerir kleift að framkvæma þetta í sölupöntun.  

[!INCLUDE[prod_short](includes/prod_short.md)] reiknar út sendingar og afhendingardaga út frá þekktum og væntanlegum lausum dagsetingum sem þú getur lofað viðskiptamönnum.  

Ef tilgreindur er afgreiðsludagsetning á sölupöntunarlínunni notar forritið þessa dagsetningu sem upphafspunkt fyrir eftirfarandi útreikninga  

- Umbeðin afgreiðsludagsetning – Flutningstími = Áætluð afhendingardagsetning  
- sfhendingardagsetning + afgr.tími vara á útl. úr vöruh. = afh.dags.  

Ef varan er tiltæk til tínslu á afhendingardagsetningu þá getur söluferlið haldið áfram. Ef varan er ekki tiltæk til tínslu á afhendingardegi þá birtist viðvörun um að varan sé uppseld.  

Ef ekki er tilgreind umbeðin afgreiðsludagsetning á sölupöntunarlínunni, eða ef ekki er hægt að verða við umbeðinni afgreiðsludagsetningu, er reiknuð fyrsta dagsetningin sem vörurnar eru tiltækar. Sú dagsetning er færð inn í reitinn **Afhendingardagsetning** á línuna og eftirtaldar reiknireglur eru síðan notaðar til að reikna út hvenær áætlað er að senda vörurnar ásamt því á hvaða degi viðskiptamaðurinn fær þær afhentar.  

- Afhendingardagsetning + afgr.tími vara á útl. úr vöruh. = Áætluð afhendingardagsetning  
- áætluð afhendingardagsetning + flutningstími = áætluð afgreiðsludagsetning  

## <a name="about-order-promising" />Um pöntun lofað

Aðgerðin Pöntunarloforð gerir kleift að lofa því að pöntun verði send eða afhent á tilteknum degi. Kerfið reiknar út hvenær vara er tiltæk eða hægt að lofa henni og það býr til pöntunarlínur fyrir þær dagsetningar sem samþykktar eru. Pöntunarloforðsaðgerðin reiknar fyrstu hugsanlegu dagsetningu fyrir sendingu eða afhendingu á vöru. Einnig eru búnar til innkaupabeiðnilínur, ef fyrst skyldi þurfa að kaupa inn eða framleiða vörurnar, fyrir dagsetningarnar sem eru samþykktar.

[!INCLUDE[prod_short](includes/prod_short.md)] notar tvö grundvallarhugtök:  

- Tiltækt að lofa (ATP)  
- Hægt að lofa (CTP)  

### <a name="available-to-promise" />Tiltækt að lofa

Tiltæk til að lofa (ATP) reiknar út dagsetningar á grundvelli frátekningarkerfisins. Hún gerir ráðstöfunarathugun á ófráteknu magni í birgðum með tilliti til áætlaðrar framleiðslu, innkaupa, flutninga og söluskila. Á grundvelli þessarar upplýsinga, reiknar [!INCLUDE[prod_short](includes/prod_short.md)] afhendingardagsetningu fyrir pöntun viðskiptamanns þar sem vörurnar eru tiltækar, annaðhvort í birgðum eða í áætluðum móttökum.  

### <a name="capable-to-promise" />Hægt að lofa

CTP-afhendingargeta notar „hvað ef“ aðstæður sem gildir aðeins um magn sem ekki erí birgðum eða á dagsettum pöntunum. Samkvæmt þessu dæmi, reiknar [!INCLUDE[prod_short](includes/prod_short.md)] út fyrstu dagsetningu þegar varan er til ef á að framleiða hana, kaupa eða flytja.

#### <a name="example" />Dæmi

Ef pöntun er til staðar fyrir 10 stykki, og 6 stykki eru til staðar í birgðum eða á dagsettum pöntunum, byggir útreikningur CTP-afhendingargetu á 4 stykkjum.

### <a name="calculations" />Útreikningar

Þegar [!INCLUDE[prod_short](includes/prod_short.md)] reiknar afhendingardagsetningu viðskiptamanns framkvæmir það tvo verkhluta:  

- Reiknar elstu dagsetninguna þegar viðskiptamaður hefur ekki beðið um sérstaka afgreiðsludagsetningu.  
- Vottar hvort afhendingardagsetningin sem viðskiptavinurinn biður um eða er lofað er raunsæ.  

Ef viðskiptamaðurinn biður ekki um sérstaka afgreiðsludagsetningu verður afhendingardagsetningin stillt á vinnudagsetninguna og ráðstöfunin verður byggð á þeirri dagsetningu. Ef varan er í birgðum reiknar [!INCLUDE[prod_short](includes/prod_short.md)] fram í tíma til að ákvarða hvenær afhenda megi pöntunina. Þetta næst með eftirfarandi formúlum:  

- Afhendingardagsetning + afgr.tími vara á útl. úr vöruh. = Áætluð afhendingardagsetning  
- Áætluð afhendingardagsetning – Flutningstími = Áætluð afgreiðsludagsetning  

[!INCLUDE[prod_short](includes/prod_short.md)] síðan er sannreynt hvort útreiknuð afhendingardagsetning er raunhæf með því að reikna aftur í tímann til að ákvarða hvenær varan verður að vera tiltæk til að standast setta dagsetningu. Þetta næst með eftirfarandi formúlum:  

- Áætluð afhendingardagsetning – Flutningstími = Áætluð afgreiðsludagsetning  
- Áætluð afhendingardagsetning - Afgreiðslutími út úr vöruhúsi + Afh.dags.  

Afhendingardagsetning er notuð til að gera til ráðstöfunarathugunina. Ef varan er tiltæk á þeim degi staðfestir [!INCLUDE[prod_short](includes/prod_short.md)] að umbeðin/lofuð afhending standist með því að stilla áætlaða afhendingardagsetningu á umbeðna/lofaða dagsetningu. Ef varan er ekki tiltæk er auðri dagsetningu skilað og þá getur pöntunarvinnslan notað CTP-virkni.  

Byggt á nýjum dagsetningum og tímum, allar tengdar dagsetningar eru reiknaðar samkvæmt reiknireglum sem lýst var fyrr í þessum kafla. CTP-útreikningurinn tekur lengri tíma en gefur nákvæmari dagsetningu þess hvenær viðskiptavinurinn gefur vænst þess að fá vöruna afhenta. Dagsetningarnar sem eru reiknaðar með CTP eru sýndar í **Áætluð afhendingardagsetning** og **Fyrsti mögulegi afhendingardagur** svæðunum á síðunni **Pöntun lofað línur**.  

Pantanavinnsla lýkur CTP-ferlinu með því að samþykkja dagsetningarnar. Þetta þýðir að áætlunarlína og frátekningarfærslan hafa verið stofnaðar fyrir vöruna fyrir reiknaðar dagsetningar til að tryggja að pöntunin sé uppfyllt.  

Auk ytri pantanaloforða sem hægt er að framkvæma á síðunni **Línur pöntunarloforða** er einnig hægt að lofa innri eða ytri afhendingardagsetningu fyrir uppskriftavörur. Frekari upplýsingar, sjá [Skoða tiltækileika vöru](inventory-how-availability-overview.md).

## <a name="to-set-up-order-promising" />Uppsetning pöntunarloforðs

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning pöntunarloforðs** og velja síðan viðkomandi tengil.  
2. Númer og tímaeiningarkóti er fært inn í reitinn **Mótfært (Tími)**. Einn af eftirfarandi kótum er valinn:  

    |Kóti|Lýsing|  
    |----------|-----------------|  
    |**d**|Almanaksdagur|  
    |**v**|Vika|  
    |**m**|Mánuður|  
    |**f**|Fjórðungur|  
    |**á**|Ár|  

    Til dæmis merkir “3v” að mótfærður tími eða frestur er þriggja vikna. Til að gefa til kynna gildandi tímabil, setjið forlið fyrir alla þessa kóta með bókstafnum “ c “. Eigi til dæmis mótfærður tími að vera yfirstandandi mánuður er fært inn **cm**.  
3. Númeraröð er færð inn í reitinn **Pöntunarloforð nr.** með því að velja línu af listanum á síðunni **Nr. röð**.  
4. Sniðmát pöntunarloforða er fært inn í reitinn **Sniðmát pöntunarloforða** með því að velja línu af listanum á síðunni **Listi yfir innkaupatillögusniðmát** .  
5. Innkaupatillögusniðmát er fært inn í reitinn **Pöntunarloforð Innkaupatillaga** með því að velja línu af listanum á síðunni **Listi yfir innkaupatillögusniðmát** .

### <a name="inbound-and-outbound-warehouse-handling-times-in-order-promising" />Afgreiðslutímar vöruhúss fyrir inn- og útleið í pöntun lofað

Ef afgreiðslutími vöruhúss þegar reiknað er út hvenær á að lofa pöntun í innkaupalínunni skal tilgreina á síðunni **Birgðauppsetning** sjálfgefinn afgreiðslutíma til að nota í sölu- og innkaupaskjölum. Einnig er hægt að færa inn ákveðna tíma fyrir hverja staðsetningu á síðunni **Birgðageymsluspjald**. 

#### <a name="to-enter-default-inbound-and-outbound-warehouse-handling-times-for-sales-and-purchase-documents" />Til að færa inn afgreiðslutíma vöruhús á inn- og útleið fyrir sölu- og innkaupaskjöl

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Uppsetning birgða** og velja síðan viðkomandi tengil.  
2. Í flýtiflipanum **Almennt**, í reitnum **Afgr.tími vara á innl. í vöruh.** og **Afgr.tími vara á útl. úr vöruh** skal færa inn dagafjöldann sem á taka með í útreikningi á því hvenær pöntunum er lofað.  

#### <a name="to-enter-inbound-and-outbound-warehouse-handling-times-on-locations" />Að færa inn afgreiðslutíma vöruhúss fyrir inn- og útleið í birgðageymslum

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Staðsetningu** og velja síðan viðkomandi tengil.  
2.  Opna skal viðeigandi birgðageymsluspjald.  
3.  Í flýtiflipanum **Vöruhús**, í reitina **Afgr.t. vara á innl. í vöruh** og **Afgr.tími vara á útl. úr vöruh** skal færa inn dagafjöldann sem á að taka með í útreikningi á hvenær pöntunum er lofað.  

> [!NOTE]  
>  Þegar innkaupapöntun er stofnuð, ef þú velur **Birgðageymslu** í reitnum **Senda til** í flýtiflipanum **Afhending og greiðsla** og velur síðan birgðageymslu í reitnum **Kóði birgðageymslu** munu reitirnir **Afgr.tími vara á útl. úr vöruh** og **Afgr.t. vara á innl. í vöruh** nota afgreiðslutímann sem tilgreindur er fyrir birgðageymsluna. Fyrir sölupantanir gildir það sama ef þú velur birgðageymslu í reitnum **Kóði birgðageymslu**. Ef enginn afgreiðslutími er tilgreindur fyrir birgðageymsluna verða reitirnir **Afgr.tími vara á útl. úr vöruh** og **Afgr.t. vara á innl. í vöruh** auðir. Ef reiturinn **Kóði birgðageymslu** er skilinn eftir auður í sölu- og innkaupaskjölum notar útreikningurinn afgreiðslutíma sem tilgreindur er á síðunni **Birgðauppsetning**.

## <a name="to-make-an-item-critical" />Varan bundin:

Áður en vara er sett inn í útreikning pöntun lofað, verður að merkja hana sem mikilvægt. Þessi uppsetning tryggir að ó-mikilvægar vörur trufli ekki útreikning pöntunarloforða.   
1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Vörur** og velja síðan viðkomandi tengil.  
2.  Viðeigandi birgðaspjald er opnað.  
3.  Á flýtiflipanum **Áætlun** skal velja svæðið **Bundið**.  

## <a name="to-calculate-an-order-promising-date" />Dagsetning pöntunarloforðs reiknuð:

1.  Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Sölupöntun** og velja síðan viðkomandi tengil.  
2.  Glugginn sölupöntun er opnaður og sölupöntunarlínurnar sem forritið á að reikna valdar.  
3.  Veldu aðgerðina **Pöntun lofað** og veldu svo aðgerðina **Pöntun lofað línur**.  
4.  Veldu línu og síðan einn af eftirfarandi valmöguleikum:  

    - Velja skal  **Tiltæki** ef kerfið á að reikna út hvaða dag varan verður fyrst tiltæk að teknu tilliti til birgða, áætlaðrar móttöku og brúttóþarfa.  
    - Velja skal  **Óhætt að lofa** ef vitað er að varan er ekki til í birgðahaldi og ef kerfið á að reikna út hvenær varan verður fyrst tiltæki með því að gefa út tillögur um endurnýjun.  
5.  Velja hnappinn **Samþykkja** til að samþykkja fyrstu tiltæku sendingardagsetningu.  

## <a name="see-related-microsoft-trainingtrainingmodulespromising-sales-order-delivery-dynamics-365-business-central" />Sjá tengda [Microsoft þjálfun](/training/modules/promising-sales-order-delivery-dynamics-365-business-central/)

## <a name="see-also" />Sjá einnig .

[Sala](sales-manage-sales.md)  
[Dagsetning útreiknings fyrir kaup](purchasing-date-calculation-for-purchases.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
