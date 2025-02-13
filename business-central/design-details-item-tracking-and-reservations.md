---
title: Hönnunarupplýsingar - vörurakning og frátekningar
description: Þetta efnisatriði fjallar um vörurakningu og frátekningar og lýsir heildarhugmyndinni á bak við valkostina tvo.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 06/15/2021
ms.author: edupont
---
# <a name="design-details-item-tracking-and-reservations" />Hönnunarupplýsingar: vörurakning g frátekningar

Samtímis notkun frátekninga og tiltekinnar vörurakningar er óalgengt, vegna þess að bæði búa til tenging milli framboðs og eftirspurnar. Nema þegar viðskiptamaður eða framleiðslustjóri óskar eftir tiltekinni lotu er sjaldnast ástæða til að taka frá birgðavörur sem þegar hafa vörurakningarnúmer fyrir tiltekna jöfnun. Þó það er hægt að taka frá vörur sem krefjast sérstakrar vörurakningar er þörf á sérstökum eiginleika til að forða framboðsárekstra á milli pantanavinnsla sem biðja um sömu röktu vörurnar.  
  
Hugmyndin um bindingu eftir áætlun tryggir ósértæk pöntun á raðnúmer eða lotunúmer lauslega fram að bókun. Á bókunartíma getur frátekningarkerfið stokkað ótilgreindar frátekningar til að tryggja að föst jöfnun sé möguleg á móti rað- eða lotunúmeri sem búið er að tína. Á meðan eru rað- eða lotunúmer gerð tiltæk fyrir sérstaka frátekningu í öðrum skjölum sem krefjast tiltekins rað- eða lotunúmers.  
  
Ótilgreind frátekning er frátekning þar sem notanda er sama hvaða vara er tínd og sérstök frátekning er hið gagnstæða.  
  
> [!NOTE]  
> Aðgerðin fyrir bindingu á eftir áætlun tengist aðeins vörum sem eru stilltar með tilgreindir vörurakningu og á aðeins við um fyrirvaran gagnvart birgðum, ekki gagnvart búnaðarpöntunum á innleið.  
  
Frátekning vörurakningarnúmera fellur í tvo flokka, eins og sýnt er í eftirfarandi töflu.  
  
|Frátekning|Description|  
|-----------------|---------------------------------------|  
|Sérstakt|Valið er sértækt rað- eða lotunúmer þegar birgðavara er tekin frá úr eftirspurn, svo sem sölupöntun.<br /><br /> Þetta er venjuleg frátekning. Það er stíft tengsl milli framboðs og eftirspurnar sem bæði bera raðnúmer eða lotunúmer. **Athugið:**  Eftirspurn ber raðnúmer eða lotunúmer. <br /><br /> Til dæmis ef taka á frá fötu af blárri málningu úr Lotu A, því viðskiptamaðurinn biður um það. Dós með blárri málningu úr lotu A er afhent viðskiptamanni.|  
|Ótilgreint|Ekki er valið sértækt rað- eða lotunúmer þegar birgðavara er tekin frá úr eftirspurn, svo sem sölupöntun.<br /><br /> Þetta er staða sem er sett á frátekningarfærsla fyrir rað- eða lotunúmer sem eru ekki tilgreind sérstaklega. **Athugið:** Eftirspurn ber ekki raðnúmer eða lotunúmer. <br /><br /> Til dæmis ef taka á frá fötu af blárri málningu úr hvaða lotu sem er í fyrir sölupöntun. Dós með blárri málningu með handahófskenndu rað- eða lotunúmeri er afhent viðskiptamanni.|  
  
Aðalmunurinn á tilgreindum og ótilgreindum frátekningum er skilgreindur með tilvist raðnúmera eða lotunúmer eftirspurnarmegin, eins og sýnt er í eftirfarandi töflu.  

| Tegund            | Framboð                | Eftirspurn                   |
|-----------------|-----------------------|--------------------------|
| **Sérstakt**    | Rað- eða lotunúmer. | Rað- eða lotunúmer.    |
| **Ekki sérstatk** | Rað- eða lotunúmer. | Ekkert rað- eða lotunúmer. |
  
Þegar þú tekur frá birgðamagn úr skjalalínu skjala á útleið fyrir vöru sem er með úthlutuð vörurakningarnúmer og er sett upp með sértæka vörurakningu leiðir síðan **Frátekning** þig í gegnum mismunandi verkflæði, allt eftir því hversu mikla þörf þú hefur fyrir rað- eða lotunúmer.  
  
## <a name="specific-reservation" />Sérstakar frátekning
Ef þú velur **Taka frá** úr línu skjala á útleið birtist svargluggi sem spyr hvort taka eigi frá sérstök rað- eða lotunúmer. Ef **Já** er valið birtist listi með öllum rað- eða lotunúmerum sem er úthlutað á skjalalínuna. Síðan **Frátekning** opnast eftir að þú velur einn af rað- eða lotunúmer, og þú getur þá frátekið meðal völdum raðnúmer eða lotunúmer á venjulegan hátt..  
  
Ef einhver af tilgreindum vörurakningarnúmerum sem reynt er að taka frá eru geymd í ótilgreindum frátekningum láta skilaboð neðst á síðunni **Frátekning** vita hversu mörg af fráteknu heildarmagni eru geymd í ótilgreindum frátekningum og hvort þau eru ennþá tiltæk.  
  
## <a name="nonspecific-reservation" />Ótilgreind frátekning
Ef **Nei** er valið í svarglugganum sem birtist opnast síðan **Frátekning** þar sem hægt er að taka frá úr öllum rað- eða lotunúmerum í birgðum.  
  
Vegna uppbyggingu frátekningarkerfisins, þegar þú setur ósértæka frátekningu um vöruskráðan hlut verður, kerfið að velja tiltekna birgðahöfuðbók til að panta gegn. Vegna þess að færslur í birgðahöfuðbók bera vörurakningarnúmer, tekur frátekningin óbeint frá tiltekin rað- eða lotunúmer, jafnvel þó að þú hafir það ekki í hyggju að. Til að höndla þetta ástand, frátekningarkerfið reynir að stokka Ósértæk frátekningarfærslur fyrir bókun.  
  
Kerfið pantar áfram gegn ákveðnum færslum en notar svo endurröðun þar sem til staðar er tiltekin eftirspurn fyrir lotunni eða raðnúmeri í ótilgreindu pöntuninni. Þetta getur verið tilfellið þegar eftirspurnafærsla er bókuð, t.d. sölupöntun, notkunarbók eða flutningspöntun, fyrir rað- eða lotunúmerið, eða þegar reynt er að taka frá rað- eða lotunúmerið. Kerfið endurskipuleggur pantanirnar til að lotan eða raðnúmerið sé í boði fyrir eftirspurnina eða tilteknu pöntunina, og setur þannig aðra lotu eða raðnúmer í ótilgreindu pöntuninni. Ef það er ekki nóg magn í birgðum endurskipuleggur kerfið eins mikið og mögulegt er, og framboðsvilla birtist ef enn er ekki nóg magn þegar bókað er.  
  
> [!NOTE]  
>  Í ótilgreindri frátekningu er reiturinn fyrir lotunúmerið eða raðnúmerið auður í frátekningarfærslunni sem vísar á eftirspurnina, svo sem salan.  
  
## <a name="reshuffle" />Stokka
Þegar notandi bókar skjal á útleið eftir að hafa tekið til rangt raðnúmer eða lotunúmer eru aðrar ótilgreindar bókanir stokkaðartil að  endurspegla raunverulegt raðnúmer eða lotunúmer sem er tekið til. Þetta uppfyllir bókunarvél með fastar jafnanir milli framboðs og eftirspurnar.  
  
Fyrir allar studdar viðskiptaaðstæður er aðeins hægt að endurraða gegn jákvæðum birgðahöfuðbókarfærslum sem eru með frátekningu og rað- eða lotunúmer en án skilgreindra rað eða lotunúmera á eftirspurnarhlið.  
  
## <a name="supported-business-scenarios" />Styður fyrirtækjaatburðarás
Aðgerðin fyrir bindingu á eftir áætlun styður við eftirfarandi fyrirtækisaðstæður:  
  
* Fært inn tilgreint rað- eða lotunúmer á skjali á útleið með ótilgreindum fyrirvara á röngu rað-eða lotunúmeri.  
* Að taka frá tiltekið rað- eða lotunúmer  
* Bókun skjals á útleið með ótilgreindri frátekningu rað- eða lotunúmers.  
  
### <a name="entering-serial-or-lot-numbers-on-an-outbound-document-with-wrong-nonspecific-reservation" />Færð inn rað- eða lotunúmer á skjali á útleið með röngum ótilgreindum fyrirvara.
Þetta er algengast af þremur aðstæðunum sem eru studdar. Í þessu tilviki er seint bindandi virkni tryggir að notandi getur slegið inn raðnúmer eða lotunúmer, sem er reyndar einvalalið, á útleið skjal sem þegar hefur ótilgreint frátekning annars raðnúmer eða lotunúmer.  
  
Til dæmis kemur þörfin fram þegar pantanavinnsla hefur fyrst gert ótilgreinda frátekningu á einhverju raðnúmeri eða lotunúmeri. Síðar þegar varan er tínd í raun úr birgðum þarf að færa tínd rað- eða lotunúmer inn á pöntun áður en hún er bókuð. Ótilgreinda fyrirvaranum er endurraðað við bókunartíma til að tryggja að hægt sé að slá inn valið rað- eða lotunúmer án þess að fyrirvarinn glatist og til að tryggja að hægt sé að nota og bóka fullkomlega valið rað- eða lotunúmer.  
  
### <a name="reserve-specific-serial-or-lot-numbers" />Taka frá tiltekin rað- eða lotunúmer
Í þessu fyrirtækjaumhverfi, tryggir binding á eftir áætlun að notandi sem er að reyna að taka frá ákveðna raðnúmer eða lotunúmer sem er nú  áskilin ótilgreint getur gert það. Ótilgreind frátekning er stokkuð við frátekningu til að losa rað- eða lotunúmer fyrir sérstaka frátekningu.  
  
Endurskipulagning er sjálfvirk en innfelld hjálp sést neðst á síðunni **Frátekning** og sýnir eftirfarandi texta:  
  
**XX af heildar- fráteknu magni eru ósértæk og kunna að vera laus.**  
  
Að auki **Ótilgreint frátekið magn** reitur sýnir hversu margir fyrirvara færslur eru ósérhæfðar. Þessi reitur er sjálfgefið ekki sýnileg notendum.  
  
### <a name="posting-an-outbound-document-with-nonspecific-reservation-of-serial-or-lot-numbers" />Bókun skjals á útleið með ótilgreindri frátekningu rað- eða lotunúmera
Þessar viðskiptaaðstæður eru studdar með aðgerðinni fyrir bindingu sem leyfir fastar umsóknir og bókanir fyrir útleið sem er tekið til með því að endurstokka aðra ótilgreinda frátekningu af rað- eða lotunúmeri. Ef endurröðun er ekki möguleg birtast eftirfarandi villuboð um staðalskekkju þegar notandi reynir að bóka afhendinguna:  
  
**Ekki er hægt að jafna vöru XX að fullu.**  
  
## <a name="see-also" />Sjá einnig
[Hönnunarupplýsingar: vörurakning](design-details-item-tracking.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
