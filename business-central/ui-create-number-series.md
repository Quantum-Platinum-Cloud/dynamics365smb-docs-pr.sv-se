---
title: "Så här skapar du nummerserier | Microsoft Docs"
description: "Lära dig hur du anger nummerserier som tilldelar unika ID-koder till konton och dokument i Business Central."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: numbers, numbering
ms.date: 03/27/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: ea9b4a6310df319df06d02c53b9d6156caaee24f
ms.openlocfilehash: 4d7e554300f0b445816ef9dd7fb81ea54fd25bf7
ms.contentlocale: sv-se
ms.lasthandoff: 03/28/2018

---
# <a name="create-number-series"></a>Skapa nummerserier
För varje företag som du lägger upp måste du tilldela unika ID-koder till exempelvis redovisningskonton, kund- och leverantörskonton, fakturor och dokument. Numrering är viktigt inte enbart för identifiering. Ett adekvat numreringssystem gör också företaget mer hanterbart och enkelt att analysera, och kan minska antalet fel som uppstår vid datainmatning.

> [!NOTE]  
>   Vi rekommenderar att du använder samma nummerserie som du ser i fönstret **Nr-serielista** i demonstrationsföretaget CRONUS. Koder som *P-INV+* kanske inte passar direkt, men [!INCLUDE[d365fin](includes/d365fin_md.md)] har flera standardinställningar som hör ihop med dessa nummerseriekoder.

Du skapar ett numreringssystem genom att skapa en eller flera koder för varje typ av huvuddata eller dokument. Du kan till exempel skapa en kod för numrering av kunder, en annan för numrering av försäljningsfakturor och en annan för numrering av dokument i redovisningsjournaler. När du har skapat en kod måste du skapa minst en nummerserierad. Nummerserieraden innehåller information som första och sista nummer i serien och startdatum. Du kan registrera flera nummerserierader per nummerseriekod, med olika startdatum på varje rad. Nummerserierna används löpande, med början på respektive startdatum.

Du ställer normalt in nummerserier till att automatiskt infoga nästa nummer på nya kort eller dokument som du skapar. Men kan du också skapa en nummerserie för att manuellt ange det nya numret. Du anger detta med kryssrytan **Manuell numrering.**

Om du vill använda mer än en nummerseriekod för en typ av huvuddata, till exempel om du vill använda olika nummerserier för olika kategorier med artiklar, kan du använda nummerseriesamband.

## <a name="behavior-of-the-no-field-on-documents-and-cards"></a>Fältet Nr. på Dokument och kort
På försäljnings-, inköps- och överföringsdokument och alla kort kan **Nr.** fyllas i automatiskt (från en nummerserie) eller manuellt, och kan även ställas in att vara osynligt.

Fältet **nr.** kan fyllas i på tre sätt:

1. Om endast en nummerserie finns för typen av dokument eller kort finns där kryssrutan **Förvalda nr.** är markerad och kryssrutan **Manuella nr.** inte är markerad, så fylls fältet automatiskt i med nästa nummer i serien, och fältet **Nr.** kommer inte att visas.

    > [!NOTE]  
    > Om nummerserien inte fungerar, till exempel eftersom antalet nummer har tagit slut, kommer fältet **Nr.** att visas och du kan manuellt ange ett nummer eller lösa problemet i fönstret **Lista för nummerserie**.

2. Om mer än en nummerserie finns för typen av dokument eller kort, och kryssrutan **Förvalda nr.** inte har markerats för den nummerserie som för tillfället tilldelats, så kommer fältet **Nr.** att visas, och du kan öppna fönstret **Lista för nummerserie** och välja den nummerserie som du vill använda. Nästa nummer i serien förs då in i fältet **Nr.** .

3. Om du inte har skapat en nummerserie för dokument- eller korttypen, eller om fältet **Manuella nr.** har valts för nummerserien, så kommer fältet **Nr.** att visas, och du måste ange en siffra manuellt. Du kan ange högst 20 tecken, både siffror och bokstäver.

När du öppnar ett nytt dokument eller kort som det finns en nummerserie för, öppnas tillhörande **Inställningar för nummerserie**-fönster så att du kan ställa in en nummerserie för den typen av dokument eller kort innan du fortsätter med övriga datainmatningar.

> [!NOTE]  
> Om du behöver aktivera manuell numrering för till exempel nya artikelkort som har skapats med en datamigreringsprocess som döljer fältet **Nr.** som standard, gå då till fönstret **Lagerinställningar** och välj sedan fältet **Artikelnr.** om du vill öppna och ange relaterade nummerserier som **Manuell numrering**.

## <a name="to-create-a-new-number-series"></a>Så här skapar du nummerserier
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Nr-serier** och välj sedan relaterad länk.
2. Välj åtgärden **Ny**.
3. Fyll i fälten på en ny rad efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]

## <a name="to-set-up-where-a-number-series-is-used"></a>Om du vill konfigurera var en nummerserie används
I följande procedur beskrivs hur du ställer in nummerserier för området Försäljning. Stegen är liknande för andra områden.
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljning & kundreskontra** och välj sedan relaterad länk.
2. I fönstret **försäljning** klickar du på snabbfliken **nr-serier** och väljer önskade nummerserier för varje försäljningskort och dokument.

Det markerade numret kommer nu att användas för att fylla i fältet **nr.** på kortet eller dokumentet i fråga enligt de inställningar du har gjort på nummerserieraden.

## <a name="to-create-relationships-between-number-series"></a>Så här skapar du samband mellan nummerserier
Om du har definierat mer än en nummerseriekod för samma typ av allmän information eller transaktioner kan du skapa samband mellan koderna. Den här funktionen gör det enklare för dig att välja bland koderna när du använder ett nummer.

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Nr-serier** och välj sedan relaterad länk.
2. Markera raden med de nummerserier som du vill skapa relationer för och välj sedan **Relationer**.
3. I fältet **Seriekod** anger du koden för nummerserien som du vill koppla till serien du valde i steg 2.
4. Lägg till en rad för varje kod som du vill koppla till den valda nummerserien.
5. Stäng fönstret.

När du hädanefter definierar något för vilket ett nummer krävs kan du använda sambanden som har skapats för att välja bland de kopplade nummerserierna.

## <a name="see-also"></a>Se även
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)  
