---
title: Sameina móttökur í einn reikning
description: Ef reikningsfæra á fleiri en eina innkaupamóttöku í einu er hægt að nota aðgerðina sameinaðar móttökur.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '136, 145, 146, 9308'
ms.date: 08/03/2022
ms.author: edupont
---
# <a name="combine-receipts-on-a-single-invoice" />Sameina móttökur í einn reikning

Ef reikningsfæra á fleiri en eina innkaupakvittun í einu er hægt að velja margar móttökulínur í innkaupareikningnum.  

Áður en hægt er að búa til sameinaða innkaupamóttöku, þarf að vera búið að bóka fleiri en eina móttöku frá sama lánardrottininn í sama gjaldmiðlinum. Það er að segja, það þarf að vera búið að fylla út tvær eða fleiri innkaupapantanir og bóka þær sem mótteknar en ekki reikningsfærðar.  

Þegar innkaupareikningar eru sameinaðir og bókaðir á reikningi, er bókaður innkaupareikningur stofnaður fyrir reikningslínu(r). Reiturinn **Reikningsfært magn** á upprunalegri innkaupapöntun eða standandi innkaupapöntun er uppfærður á grundvelli reikningsfærða magnsins. Hins vegar er upprunalega innkaupaskjalinu ekki eytt jafnvel þó það hafi verið móttekið og reikningsfært að fullu og því verður að eyða innkaupaskjalinu.  

> [!NOTE]
> Ekki er hægt að leiðrétta eða hætta við innkaupareikninginn síðar. Ef ætlunin er að breyta innkaupareikningi sem er búinn til á þennan hátt verður að nota innkaupakreditreikninga. Nánari upplýsingar er að finna [Ógreiddir innkaupareikningar leiðréttir eða afturkallaðir](purchasing-how-correct-cancel-unpaid-purchase-invoices.md).

## <a name="to-combine-receipts" />Sameining móttakna:

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Innkaupareikningar** og velja síðan viðkomandi tengil.  
2. Valið er **Nýtt** aðgerð. Nánari upplýsingar eru í reitnum [Skrá innkaup](purchasing-how-record-purchases.md).  
3. Á flýtiflipanum **Línur** skal velja **Sækja móttökulínur** aðgerðina.  
4. Nokkrar móttökulínur eru valdar sem eiga að vera á reikningnum:  

    Ef röng móttökulína var valin eða byrja á upp á nýtt er einfaldlega hægt að eyða línunum í innkaupareikningum og nota aftur aðgerðina **Sækja móttökulínur**.  
5. Til að bóka reikningur er valið aðgerðin **bóka**.  

## <a name="to-remove-open-purchase-orders-after-combined-receipt-posting" />Til að fjarlægja opnar innkaupapantanir eftir bókun sameinaðrar móttöku

1. Veldu ![Ljósapera sem opnar eiginleika Viðmótsleitar.](media/ui-search/search_small.png "Segðu mér hvað þú vilt gera") táknið, fara í **Eyða reiknf. innkaupapöntunum** og velja síðan viðkomandi tengil.  
2. Fyllið inn í reitina eftir þörfum. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)].
3. Velja hnappinn **Í lagi**.  

Að öðrum kosti skal eyða einstökum pöntunum handvirkt.

Skref 1 til 3 eru endurtekin fyrir öll skjöl sem urðu fyrir áhrifum, eins og auðar innikaupapantanir.

## <a name="see-related-microsoft-trainingtrainingmodulesprocessing-invoices-dynamics-365-business-central" />Sjá tengda [Microsoft þjálfun](/training/modules/processing-invoices-dynamics-365-business-central/)

## <a name="see-also" />Sjá einnig .

[Innkaup](purchasing-manage-purchasing.md)  
[Leiðrétta eða afturkalla ógreidda innkaupareikninga](purchasing-how-correct-cancel-unpaid-purchase-invoices.md)  
[Vinna með [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
