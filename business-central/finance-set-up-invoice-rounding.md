---
title: Ställa in överavrundning
description: 'Om du måste avrunda fakturabelopp när du skapar fakturor, kan du använda funktionen för automatisk avrundning som förklaras här.'
author: brentholtorf
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: '5, 16, 118, 459, 460, 495'
ms.date: 06/16/2021
ms.author: bholtorf
---
# <a name="set-up-invoice-rounding" />Ställa in överavrundning
Om du måste avrunda fakturabelopp när du skapar fakturor, kan du använda funktionen för automatisk avrundning. När en faktura rundas av infogas en extra rad med avrundningsbeloppet och bokförs tillsammans med övriga fakturarader.

> [!NOTE]  
>  Lokala regler eller lokal praxis kanske kräver att fakturan rundas av på ett visst sätt, till exempel till ett belopp som är delbart med 0,05.  

För att kunna använda den automatiska fakturaavrundningen måste du:  

* ange vilka redovisningskonton som differenserna ska bokföras på.  
* ange regler för fakturaavrundning i lokal valuta och i utländsk valuta.  
* aktivera funktionen.  

> [!NOTE]  
>  Förutom fakturaavrundningsfunktionen kan belopp på fakturor rundas av med funktionerna A-pris avrundning och Belopp avrundning.  

## <a name="set-up-general-ledger-accounts-for-invoice-rounding-differences" />Så här skapar du redovisningskonton för avrundningsdifferenser av fakturor
Om du vill använda programmets funktion för automatisk avrundning av fakturabelopp måste du först upprätta redovisningskonton eller konton där avrundningsskillnaderna bokförs. Innan du kan göra detta måste du definiera produktbokföringsmallar för moms. Mer information finns i [Ange moms](finance-setup-vat.md).  

### <a name="to-set-up-general-ledger-accounts-for-invoice-rounding-differences" />Så här skapar du redovisningskonton för avrundningsdifferenser av fakturor
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **kontoplan** och väljer sedan relaterad länk.  
2. På sidan **Kontoplan** ställer du in kontot och kallar det för **Faktura avrundning** eller något liknande. [!INCLUDE[prod_short](includes/prod_short.md)] använder kontonamnet som text för de fakturor som avrundas.  
3. Beroende på om du använder moms eller omsättningsskatt väljer du i fälten **Omsättn. skatt produktbokföringsmall** eller **Moms produktbokföringsmal** och väljer en bokföringsmall för avrundade belopp. Du vill kanske skapa en ny gruppkod som kan användas för fakturaavrundning.
4. Lämna fälten **Typ av bokföring**, och antingen **Omsättn. skatt rörelsebokföringsmall** eller **Moms rörelsebokföringsmall** tomma. <!-- Why do we say to leave these blank, when there are a lot of other fields we also leave blank but don't mention? -->  

Nu kan du koppla fakturaavrundningskontot till bokföringsmallar på sidan **Leverantörsbokföringsmallar**.  <!-- Why only the vendor posting groups? -->

## <a name="set-up-rounding-for-foreign-and-local-currencies" />Så här anger du avrundningsregler för utländska valutor
Innan du kan använda den automatiska fakturaavrundningsfunktionenmåste du ställa in avrundningsregler för utländsk och lokal valuta.

### <a name="to-set-up-rounding-for-foreign-currencies" />Så här anger du avrundningsregler för utländska valutor:
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") anger du **Valutor** och väljer sedan relaterad länk.  
2. På sidan **valutor** väljer du valutan för att öppna **valutakort**, och fyller sedan i fälten **Belopp avrundning**, **A-pris avrundning**, **Faktura avrundning** och **Avrundningstyp**.

### <a name="to-set-up-rounding-for-your-local-currency" />Så här anger du avrundningsregler för den lokala valutan:
1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Redovisningsinställningar** och välj sedan relaterad länk.  
2. På sidan **Redovisningsinställningar** på snabbfliken **Allmänt** fyller du i fälten **Faktura avrundning** och **Avrundningstyp**.  

## <a name="activate-the-invoice-rounding-function" />Så här aktiverar du funktionen Avrunda fakturabelopp
För att se till att försäljnings- och inköpsfakturor avrundas automatiskt aktiverar du funktionen Avrunda fakturabelopp. Du kan aktivera fakturaavrundningen separat för försäljnings- och inköpsfakturor.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta vad du vill göra") ange **Försäljningsinställningar** eller **Inköpsinställningar**, och välj sedan relaterad länk.  
2. På snabbfliken **Allmänt**, välj kryssrutan **Öresutjämning**.  

## <a name="see-also" />Se även
[Fakturaförsäljning](sales-how-invoice-sales.md)  
[Registrera inköp](purchasing-how-record-purchases.md)


[!INCLUDE[footer-include](includes/footer-banner.md)]
