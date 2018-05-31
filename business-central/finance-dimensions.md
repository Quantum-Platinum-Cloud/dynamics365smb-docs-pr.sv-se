---
title: Arbeta med Dimensioner | Microsoft Docs
description: "Du kan använda dimensioner för att kategorisera poster, till exempel efter avdelning eller projekt, så att du kan spåra och analysera data."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: analysis, history, track
ms.date: 01/25/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 349a4d54a95999e3e2c2b19cc2a40c2dd1afd445
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="working-with-dimensions"></a>Arbeta med dimensioner
Du kan använda dimensioner för att göra det enklare att analysera dokument såsom försäljningsorder. Dimensioner är attribut och värden som kategoriserar transaktioner så att du kan spåra och analysera dem. Dimensioner kan till exempel ange vilket projekt eller vilken avdelning en transaktion kom ifrån.  

T.ex. kan du använda dimensioner i stället för att skapa separata redovisningskonton för varje avdelning och projekt. Detta ger stora möjligheter för analys, utan att skapa en komplicerad kontoplan. Mer information finns i [Affärsstöd](bi.md).

Ett annat exempel är att ställa in en dimension kallad *Avdelning* och använda denna dimension när du bokför försäljningsdokument. Det gör att du kan använda business intelligence-verktyg för att visa vilken avdelning som sålt vilka artiklar.
Ju fler dimensioner du använder, desto mer detaljerade rapporter kan du baseras dina affärsbeslut på. En enda försäljningstransaktion kan till exempel innehålla olika dimensionsinformation som t.ex.:  

* Kontot som artikeln bokfördes till  
* Var artikeln såldes
* Vem som sålde den
* Vilken typ av kund som köpte den  

## <a name="analyzing-by-dimensions"></a>Analys per dimension
Funktionen dimensioner spelar en viktig roll i affärsstöd, exempelvis när du definierar analysvyer. Mer information finns i [Analysera data efter dimension](bi-how-analyze-data-dimension.md).

> [!TIP]
> Som ett snabbt sätt att analysera transaktionsdata med dimensioner kan du filtrera summorna i kontoplanen och posterna i alla fönstrer för **Transaktioner** per dimension. Sök efter åtgärden **Ange dimensionsfilter**.

## <a name="dimension-sets"></a>Dimensionsuppsättningar
En dimensionsuppsättning en är en unik kombination av dimensionsvärden. Den lagras som dimensionsuppsättningstransaktioner i databasen. Varje dimensionsuppsättningstransaktion representerar ett enstaka dimensionsvärde. Dimensionsuppsättningen identifieras av ett gemensamt dimensionsuppsättnings-ID som tilldelats varje dimensionsuppsättningstransaktion som tillhör dimensionsuppsättningen.  

När du skapar en journalrad, dokumenthuvud eller dokumentrad kan du ange en kombination av dimensionsvärden. I stället för att uttryckligen lagra varje dimensionsvärde i databasen tilldelas ett dimensionsuppsättnings-ID till journalraden, dokumenthuvudet eller dokumentraden för att specificera dimensionsuppsättningen.  

## <a name="setting-up-dimensions"></a>Lägga upp dimensioner
Du kan ange de dimensioner och dimensionsvärden för att kategorisera journaler och dokument, till exempel försäljningsorder och inköpsorder. Du ställer in dimensioner i fönstret **Dimensioner** där du skapar en rad för varje dimension som t.ex. *Projekt*, *Avdelning*, *Område* och *Säljare*.

Du kan också ställa in värden för dimensioner. Värden kan till exempel vara avdelningarna i företaget. Dimensionsvärden kan anges i en hierarkisk struktur som liknar kontoplanen, så att data kan brytas ned i olika detaljeringsgrader och delmängder av dimensionsvärden kan räknas samman. Du kan definiera så många dimensioner och dimensionsvärden som behövs och alla i företaget kan använda dem.

Du kan också ställa in vissa globala dimensioner och genvägsdimensioner:  

* **Globala dimensioner** används som filter, till exempel i rapporter och batch-jobb. Du kan använda två globala dimensioner, så välj dimensionerna som du ofta använder.
* **Genvägsdimensioner** är tillgängliga som fält på journal- och dokumentrader. Du kan skapa upp till sex av dessa.  

### <a name="setting-up-default-dimensions-for-customers-vendors-and-other-accounts"></a>Konfigurera standarddimensioner för kunder, leverantörer och andra konton
Du kan tilldela en standarddimension för ett enskilt konto. Dimensionen kopieras till journal eller dokument när du ange numret på en rad, men du kan ta bort eller ändra koden på raden om det behövs. Du kan också göra en dimension obligatorisk för att bokföra en transaktion med en viss typ av konto.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Dimensioner** och välj sedan relaterad länk.  
2.  I fönstret **Dimensioner** väljer du relevant dimension och sedan åtgärden **Standarddim. för kontotyp**.  
4.  Fyll i en rad för varje ny standarddimension du vill ange. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

> [!TIP]  
>  Om du vill att en dimension ska vara obligatorisk men du inte vill tilldela ett standardvärde till den, lämnar du fältet **Dimensionsvärdekod** tomt och markerar **Kod alltid** i fältet **Bokförs med**.  

> [!WARNING]  
>  Om kontot ska användas i batch-jobbet **Justera valutakurser** eller i batch-jobbet **Bokför lagerkostnad i redov.konto**, välj då inte **Kod obligatoriskt** eller **Samma kod**. Det går inte att använda dimensionskoder i dessa batch-jobb.  

> [!NOTE]  
>  Om en annan dimension än den standarddimension som definierats för kontotypen ska kopplas till ett konto måste en standarddimension anges för kontot. På så sätt ersätter standarddimensionen för det enskilda kontot standarddimensionen för kontotypen.  

### <a name="to-set-up-default-dimension-priorities"></a>Så här anger du standarddimensionsprioritet  
Olika kontotyper, t.ex. ett kundkonto och ett artikelkonto, kan ha olika definierade standarddimensioner. Detta kan resultera i att flera standarddimensioner för en dimension föreslås för en transaktion. Du kan undvika att den här typen av konflikter uppstår genom att använda prioritetsregler för de olika källorna.  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Prioriteringar för standarddimension** och välj sedan relaterad länk.  
2.  I fönstret **Standard dimensionsprioritet** i fältet **Källkod** anger du ursprungskoden för den transaktionstabell som standarddimensionsprioriteten.  
3.  Fyll i en rad för varje standarddimensionsprioritet du vill ha för den valda ursprungskoden.
4.  Upprepa proceduren för varje ursprungskod du vill ange standarddimensionsprioritet för.  

> [!IMPORTANT]  
>  Om du definierar två tabeller med samma prioritet för samma ursprungskod använder [!INCLUDE[d365fin](includes/d365fin_md.md)] automatiskt tabellen med lägst tabell-ID.  

### <a name="to-set-up-dimension-combinations"></a>Så här definierar du dimensionskombinationer  
Du kan förhindra att transaktioner bokförs med oförenliga eller irrelevanta dimensioner genom att spärra eller begränsa vissa kombinationer av två dimensioner. En spärrad dimensionskombination innebär att du inte kan bokföra båda dimensionerna i samma transaktion, oberoende av dimensionsvärdena. En begränsad dimensionskombination innebär att du kan bokföra båda dimensionerna i samma transaktion, men endast för vissa kombinationer av dimensionsvärden.

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Dimensionskombinationer** och välj sedan relaterad länk.  
2.  I fönstret **Dimensionskombinationer** och välj något av följande alternativ i fönstret  

    |Fält|Description|
    |----------------------------------|---------------------------------------|  
    |**Inga begränsningar**|Den här dimensionskombinationen har inga begränsningar. Alla dimensionsvärden är tillåtna.|  
    |**Begränsad**|Den här dimensionskombinationen är begränsad beroende på vilka dimensionsvärden som anges. Du definierar begränsningarna i fönstret **Dimensionsvärdekombination**.|  
    |**Spärrad**|Den här dimensionskombinationen är inte tillåten.|  

3.  Om du valde alternativet **Begränsad** måste du definiera vilka kombinationer av dimensionsvärden som är spärrade. Gör det genom att välja fältet för att definiera dimensionskombinationen.  
4.  Välj en dimensionsvärdekombination som är spärrad och ange **Spärrad** i fältet. Ett tomt fält innebär att dimensionsvärdekombinationen är tillåten. Upprepa i fall flera kombinationer är spärrade.  

> [!NOTE]  
>  Samma dimensioner visas både på rader och i kolumner vilket innebär att alla dimensionskombinationer visas två gånger. [!INCLUDE[d365fin](includes/d365fin_md.md)] visar inställningarna automatiskt i båda fälten. Du kan inte välja någonting i fälten från det övre vänstra hörnet och nedåt eftersom dessa fält har samma dimension både på rader och i kolumner.  
>   
>  Det alternativ du valt visas inte förrän markören flyttas ur fältet.  
>   
>  Om du vill visa namnet på dimensionerna i stället för koden markerar du fältet **Visa kolumnnamn**.

### <a name="getting-an-overview-of-dimensions-used-multiple-times"></a>Få en översikt över dimensioner som används flera gånger
Fönstret **Standarddimensioner: Flera** anger hur en grupp konton använder dimensioner och dimensionsvärden. Det gör du genom att markera flera konton och sedan ange standarddimensioner och standarddimensionsvärden för alla konton som du har markerat i listan över konton. När du anger standarddimensioner för de markerade kontona föreslås dessa dimensioner och dimensionsvärden varje gång något av kontona används, exempelvis på en journalrad. På så sätt underlättas användarens arbete med att registrera transaktioner, detta eftersom dimensionsfälten fylls i automatiskt. De dimensionsvärden som föreslås kan dock ändras, till exempel på en journalrad.

Fönstret **Standarddimensioner: Flera** innehåller följande fält:
|Fält|Description|
|----------------------------------|---------------------------------------|  
|**Dimensionskod**|Visar alla dimensioner som har definierats som standarddimensioner för ett eller flera av de markerade kontona. Om du väljer fältet kan du se en lista över tillgängliga dimensioner. Om du väljer en dimension anges den valda dimensionen som standarddimension för alla markerade konton.|
|**Dimensionsvärdekod**|Visar antingen ett enstaka dimensionsvärde eller termen (Konflikt). Om ett dimensionsvärde visas i fältet har alla markerade konton samma standarddimensionsvärde för en dimension. Om termen (Konflikt) visas i fältet har inte alla markerade konton samma standarddimensionsvärde för en dimension. Om du väljer fältet kan du visa en lista över alla tillgängliga dimensionsvärden för en dimension. Om du väljer ett dimensionsvärde anges det valda dimensionsvärdet som standarddimensionsvärde för alla markerade konton.|
|**Bokförs med**|Visar antingen en enstaka bokföringsregel eller termen (Konflikt). Om en bokföringsregel visas i fältet har alla markerade konton samma bokföringsregel för ett dimensionsvärde. Om termen (Konflikt) visas i fältet har inte alla markerade konton samma bokföringsregel för ett dimensionsvärde. Om du väljer fältet Bokförs med kan du visa en lista över bokföringsregler. Om du markerar en bokföringsregel tillämpas den på alla markerade konton.|

### <a name="example-of-dimension-setup"></a>Exempel på dimensionsinställningarna
Anta att ditt företag vill spåra transaktioner utifrån organisationens struktur och geografiska platser. För att göra detta kan du ange två dimensioner i fönstret **Dimensioner**:

* **OMRÅDE**  
* **AVDELNING**  

| Kod | Name | Kodledtext | Filterledtext |
| --- | --- | --- | --- |
| OMRÅDE |Område |Områdeskod |Analysfilter |
| AVDELNING |Avdelning |Avdelningskod |Avdelningsfilter |

För **OMRÅDE**, lägger du till följande dimensionsvärden:

| Kod | Name | Dimensionsvärdetyp |
| --- | --- | --- |
| 10 |Amerika |Från-summa |
| 20 |Nordamerika |Standard |
| 30 |Stillahavsområdet |Standard |
| 40 |Sydamerika |Standard |
| 50 |Amerika, hela |Till-summa |
| 60 |Europa |Från-summa |
| 70 |EU |Standard |
| 80 |Utanför EU |Standard |
| 90 |Europa totalt |Till-summa |

För de två huvudsakliga geografiska områdena, USA och Europa, lägger du till underkategorier för områden med indrag av dimensionsvärden. Då kan du rapportera på försäljning eller utgifter i områden och hämta summorna för de större geografiska områdena. Du kan även välja att använda länder eller regioner som dimensionsvärden, eller länder eller orter, beroende på ditt företag.  
> [!NOTE]  
>   Om du vill upprätta en hierarki måste koderna vara i alfabetisk ordning. Det innefattar koderna för dimensionsvärdena som ges i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

För **AVDELNING**, lägger du till följande dimensionsvärden:

| Kod | Name | Dimensionsvärdetyp |
| --- | --- | --- |
| ADMIN |Administration |Standard |
| PROD |Produktion |Standard |
| FÖRS |FÖRS |Standard |

Med detta inställt lägger du sedan till två dimensioner som de två globala dimensionerna i fönstret **Redovisningsinställningar**. Det betyder att du kan använda OMRÅDE och AVDELNING som filter för redovisningstransaktioner, samt i alla rapporter och kontouppställningar. De båda globala dimensionerna blir dessutom automatiskt tillgängliga för att användas som genvägsdimensioner på transaktionsrader och i dokumenthuvuden.  

## <a name="using-dimensions"></a>Använda dimensioner
I ett dokument som t.ex. en försäljningsorder kan du lägga till dimensionsinformation för både en individuell dokumentrad och själva dokument. T.ex. i fönstret **Försäljningsorder** kan du ange dimensionsvärden för de två första genvägsdimensionerna på den individuella försäljningsraden och du kan lägga till ytterligare dimensionsinformation om du väljer knappen **Dimensioner**.  

Om du istället arbetar med en journal kan du lägga till dimensionsinformation i en transaktion om du har lagt upp genvägsdimensioner som fält direkt på journalraderna.  

Du kan ställa in standarddimensioner för konton eller kontotyper, så att dimensioner och dimensionsvärden fylls i automatiskt.

## <a name="to-view-global-dimensions-in-ledger-entry-windows"></a>Så här visar du globala dimensioner i transaktionsfönster  
Globala dimensioner är alltid \-definierade och namngivna utifrån företaget. Om du vill visa de globala dimensionerna för ditt företag öppnar du fönstret **Redovisningsinställningar**.  

Du kan se om det finns globala dimensioner för transaktionerna i ett transaktionsfönster. De två globala dimensionerna skiljer sig från övriga dimensioner eftersom de kan användas som filter var som helst i [!INCLUDE[d365fin](includes/d365fin_md.md)].  

1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Kontoplan** och välj sedan relaterad länk.  
2.  I fönstret **Kontoplan** väljer du åtgärden **Redovisningstransaktioner**.  
3.  Om du bara vill visa relevanta transaktioner definierar du ett eller flera filter i fönstret.  
4.  Om du vill visa alla dimensioner för en transaktion markerar du transaktionen väljer sedan åtgärden **Dimensioner**.  

> [!NOTE]  
>  I fönstret **Transaktionsdimensioner** visas dimensionerna för en transaktion i taget. När du bläddrar bland transaktionerna ändras innehållet i fönstret **Transaktionsdimensioner** därefter.  

## <a name="see-also"></a>Se även
[Affärsstöd](bi.md)  
[Ekonomi](finance.md)  
[Analysera data efter dimensioner](bi-how-analyze-data-dimension.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
