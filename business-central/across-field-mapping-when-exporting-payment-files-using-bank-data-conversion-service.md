---
title: Reitavörpun fyrir útflutning bankagreiðsluskráa | Microsoft Docs
description: 'Þegar þú flytur út greiðsluskrár með AMC Banking 365 Fundamentals viðbótinni, mun sá sem veitir umskráningarþjónusta fyrir bankagögn geta séð eitthvað af gögnunum.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="field-mapping-when-exporting-payment-files-using-the-amc-banking-365-fundamentals-extension" />Reitarvörpun við útflutning greiðsluskrá með AMC Banking 365 Fundamentals viðbótinni
Þegar þú flytur út greiðsluskrár með AMC Banking 365 Fundamentals viðbótinni, mun sá sem veitir umskráningarþjónusta fyrir bankagögn geta séð eitthvað af gögnunum. Þjónustuveita er ábyrg fyrir persónuvernd gagnanna. Frekari upplýsingar um AMC Banking 365 Fundamentals-viðbótina er að finna í [Nota AMC Banking 365 Fundamentals viðbótina](ui-extensions-amc-banking.md).  

> [!CAUTION]  
>  Þegar þú flytur út greiðsluskrár með AMC Banking 365 Fundamentals viðbótinni, mun sá sem veitir þjónustuna geta séð eitthvað af gögnunum. Þjónustuveita, AMC Consult A/S, er ábyrg fyrir persónuvernd gagnanna. Nánari upplýsingar er að finna í [AMC-persónuverndarstefnu](https://go.microsoft.com/fwlink/?LinkId=510158).  

> [!NOTE]
> Í almenn útgáfa af [!INCLUDE[prod_short](includes/prod_short.md)], er altæk þjónustuveita til að umbreyta bankagögnum í annað skráarsnið sem bankinn krefst að er uppsett og tengt. Í norður-amerískum útgáfum má nota sömu þjónustu til að senda greiðsluskrár sem rafræna millifærslu (EFT), t.d. kerfi rafrænnar greiðslumiðlunar sem er oft notuð, en með örlítið öðruvísi leiðum.

Eftirfarandi tafla inniheldur lista yfir reiti í [!INCLUDE[prod_short](includes/prod_short.md)] þaðan sem hægt er að flytja út gögn.  

|Varpaður reitur|Reitur í töflu|Tafla|Description|  
|------------------|--------------------|-----------|---------------------------------------|  
|Númer lánveitanda|Númer lánveitanda|Bankareikningur|Kennimerki tengt við fyrirtækið þitt af bankanum til að taka við greiðslum|  
|Bankareikningsnúmer sendanda|Númer bankareiknings/IBAN|Bankareikningur|Bankareikningsnúmer (IBAN eða annað) fyrirtækisins þíns sem er tilgreint á bankareikningsspjaldinu|  
|Greiðslumiðlunarstaðall banka sendanda|Greiðslumiðlunarstaðall banka|Bankareikningur|Bankareikningsskrá notuð fyrir bankareikning sendanda|  
|Greiðslumiðlunarkóði sendibanka|Greiðslumiðlunarkóði banka|Bankareikningur|Kennimerki bankareiknings sendanda tengdur skráðum bankanöfnum sem eru notuð|  
|BIC-númer sendanda|SWIFT-númer|Bankareikningur|SWIFT-auðkenni bankareiknings sendanda|  
|Gjaldmiðill reiknings sendibanka|Gjaldmiðilskóti|Bankareikningur|Gjaldmiðilskóði reiknings sendanda|  
|Númer fylgiskjals|Númer fylgiskjals|Almenn færslubókarlína|Skjalanúmer greiðslulínunnar|  
|Jafnað við Nr. utanaðk. skjals|Jafnað við Nr. utanaðk. skjals|Almenn færslubókarlína|Ytra skjalanúmer reiknings eða kreditreiknings sem greiðslulínan er jöfnuð við|  
|Auðkenni viðtakanda|Reikningur nr.|Almenn færslubókarlína|Númer viðskiptamannsins eða lánardrottins sem er tilgreint á greiðslulínunni|  
|Tegund greiðslu|Greiðslugerð bankagagnaumreiknings|Greiðsluháttur|Gerð bankafærslu, t.d. innanlands eða alþjóðleg|  
|Greiðslutilvísun|Greiðslutilvísun|Almenn færslubókarlína|Greiðslutilvísun greiðslulínunnar|  
|Heimilisfang viðtakanda|Aðsetur|Viðskiptamaður/Lánardrottinn|Heimilisfang viðtakanda sem er tilgreint á spjaldi viðskiptamanns eða lánardrottins|  
|Borg viðtakanda|Bær|Viðskiptamaður/Lánardrottinn|Borg viðtakanda sem er tilgreind á spjaldi viðskiptamanns eða lánardrottins|  
|Nafn viðtakanda|Heiti|Viðskiptamaður/Lánardrottinn|Nafn viðtakanda sem er tilgreint á spjaldi viðskiptamanns eða lánardrottins|  
|Lands-/svæðisnúmer viðtakanda|Lands-/svæðiskóti|Viðskiptamaður/Lánardrottinn|Lands-/svæðisnúmer viðtakanda sem er tilgreint á spjaldi viðskiptamanns eða lánardrottins|  
|Póstnúmer viðtakanda|Póstnúmer|Viðskiptamaður/Lánardrottinn|Póstnúmer viðtakanda sem er tilgreint á spjaldi viðskiptamanns eða lánardrottins|  
|Bankareikningsnúmer viðtakanda|Númer bankareiknings/IBAN|Bankareikningur viðskiptamanns/Bankareikningur lánardrottins|Bankareikningsnúmer (IBAN eða annað) viðtakanda sem er tilgreint á bankareikningsspjaldi viðskiptamanns eða lánardrottins|  
|Greiðslumiðlunarkóði móttökubanka|Greiðslumiðlunarstaðall banka|Bankareikningur viðskiptamanns/Bankareikningur lánardrottins|Bankareikningsskrá notuð fyrir bankareikning viðtakanda|  
|Greiðslumiðlunarstaðall móttökubanka|Greiðslumiðlunarkóði banka|Bankareikningur viðskiptamanns/Bankareikningur lánardrottins|Kennimerki bankareiknings viðtakanda tengdur skráðum bankanöfnum sem eru notuð|  
|Netfang viðtakanda|Tölvupóstur|Viðskiptamaður/Lánardrottinn|Netfang viðtakandans|  
|Skilaboð til viðtakanda 1|Skilaboð til viðtakanda|Almenn færslubókarlína|Skilaboð til viðtakanda sem er tilgreindur á greiðslulínunni|  
|Upphæð|Upphæð|Almenn færslubókarlína|Upphæð greiðslulínunnar|  
|Gjaldmiðilskóti|Gjaldmiðilskóti|Almenn færslubókarlína|Gjaldmiðilskóði á greiðslulínunni|  
|Færsludagur|Bókunardags.|Almenn færslubókarlína|Bókunardagsetning greiðslulínunnar|  
|Reikningsupphæð|Upphafleg upphæð|Viðskiptamaður/Færsla í lánardrottnabók|Tilgreinir upphæð á færslu sem greiðslan er jöfnuð við|  
|Reikningsdagsetning|Dags. fylgiskjals|Viðskiptamaður/Færsla í lánardrottnabók|Tilgreinir reikningsdagsetningu á færslu sem greiðslan er jöfnuð við|  
|Bankaaðsetur viðtakanda|Aðsetur|Bankareikningur viðskiptamanns/Bankareikningur lánardrottins|Heimilisfang bankareiknings viðtakanda sem er tilgreint á bankareikningsspjaldi viðskiptamanns eða lánardrottins|  
|Heimilisfang bankareiknings viðtakanda sem er tilgreint á bankareikningsspjaldi viðskiptamanns eða lánardrottins|Bær|Bankareikningur viðskiptamanns/Bankareikningur lánardrottins|Borg bankareiknings viðtakanda sem er tilgreind á bankareikningsspjaldi viðskiptamanns eða lánardrottins|  
|Bankaheiti viðtakanda|Heiti|Bankareikningur viðskiptamanns/Bankareikningur lánardrottins|Nafn bankareiknings viðtakanda sem er tilgreint á bankareikningsspjaldi viðskiptamanns eða lánardrottins|  
|Land/svæði banka viðtakanda|Lands-/svæðiskóti|Bankareikningur viðskiptamanns/Bankareikningur lánardrottins|Land/svæði bankareiknings viðtakanda sem er tilgreint á bankareikningsspjaldi viðskiptamanns eða lánardrottins|  
|Póstnúmer viðtökubanka|Póstnúmer|Bankareikningur viðskiptamanns/Bankareikningur lánardrottins|Póstnúmer bankareiknings viðtakanda sem er tilgreint á bankareikningsspjaldi viðskiptamanns eða lánardrottins|  
|Heimilisfang sendibanka|Aðsetur|Bankareikningur|Heimilisfang bankareiknings sendanda sem er tilgreint á bankareikningsspjaldi|  
|Borg sendibanka|Bær|Bankareikningur|Borg bankareiknings sendanda sem er tilgreind á bankareikningsspjaldi|  
|Nafn sendibanka|Heiti|Bankareikningur|Nafn bankareiknings sendanda sem er tilgreint á bankareikningsspjaldi|  
|Land/svæði sendibanka|Lands-/svæðiskóti|Bankareikningur|Land/svæði bankareiknings sendanda sem er tilgreint á bankareikningsspjaldi|  
|Póstnúmer sendibanka|Póstnúmer|Bankareikningur|Póstnúmer bankareiknings sendanda sem er tilgreint á bankareikningsspjaldi|  
|Sniðmát almennrar færslubókar|Heiti bókarsniðmáts|Almenn færslubókarlína|Sniðmát færslubókar sem er notað fyrir greiðslulínuna|  
|Heiti færslubókarkeyrslu|Heiti bókarkeyrslu|Almenn færslubókarlína|Runuheiti færslubókar sem er notuð fyrir greiðslulínuna|  
|Nafn sendibanka - umreikningur gagna|Nafn banka – gagnaumreikn.|Bankareikningur|Nafn bankareiknings sendanda sem er áskilið af AMC Banking 365 Fundamentals tilgreint á bankareikningsspjaldinu|  

## <a name="see-also" />Sjá einnig
[Setja upp gagnaskipti](across-set-up-data-exchange.md)  
[Rafræn gagnaskipti](across-data-exchange.md)
[Nota AMC Banking 365 Fundamentals viðbótina](ui-extensions-amc-banking.md)   
[Greiða með AMC Banking 365 Fundamentals viðbótinni eða SEPA-kreditfærslu](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md)   


[!INCLUDE[footer-include](includes/footer-banner.md)]
