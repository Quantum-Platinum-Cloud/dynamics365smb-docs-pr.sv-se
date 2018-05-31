---
title: "Skapa ett försäljningsfaktura eller försäljningsorder | Microsoft Docs"
description: "Beskriver hur du skapar en pantförskrivning eller försäljningsfaktura eller försäljningsorder för att registrera ditt avtal med en kund om att sälja eller handla med produkter som omfattas av särskilda villkor."
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: bill, sale, invoice, order
ms.date: 03/12/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: f03cc11b5d8cb349567138604857ad3a679967cf
ms.openlocfilehash: 34c5b47885e82e6dc2985fabb8a4c202ede9c0f9
ms.contentlocale: sv-se
ms.lasthandoff: 04/03/2018

---
# <a name="invoice-sales"></a>Fakturaförsäljning
Du kan skapa en försäljningsfaktura eller försäljningsorder för att registrera en överenskommelse med en kund om att sälja vissa produkter till vissa leverans- och betalningsvillkor.  

Det finns två situationer där du måste använda en försäljningsorder i stället för en faktura:  

* Om du behöver skicka en del av en orderkvantitet, till exempel eftersom den fullständiga kvantiteten inte är tillgänglig.  
* Om du säljer artiklar som leverantören levererar direkt till kunden, kallat direktleverans. För mer information finns i [Utföra direktleveranser](sales-how-drop-shipment.md).  

I alla andra aspekter fungerar försäljningsorder och försäljningsfakturor på samma sätt. Mer information finns i [Sälja produkter](sales-how-sell-products.md).

Du kan förhandla med kunden genom att först skapa förs.offerter, som du kan omvandla till en försäljningsfaktura när du instämmer om försäljningen. Mer information finns i [Skapa erbjudanden](sales-how-make-offers.md).

Om kunden bestämmer sig att köpa kan du bokföra fakturan för att skapa relaterade kvantitet- och värdetransaktioner. När du bokför försäljningsfakturan, kan du också e-posta dokument som en PDF-bilaga. Du kan använda ifylld e-postbrödtext med en sammanfattning av fakturan och betalningsinformationen, till exempel en länk till PayPal. Mer information finns i [Skicka dokument via e-post](ui-how-send-documents-email.md).

I affärsmiljöer där kunden måste betala för produkter i förväg måste du vänta på kvittot på betalning innan du levererar produkterna. I de flesta fall behandlar du inkommande betalningar några veckor efter leverans, genom att koppla betalningarna till dess relaterade obetalda bokförda försäljningsfakturor. Mer information finns i [Stämma av betalningar genom att använda automatisk koppling](receivables-how-reconcile-payments-auto-application.md).

I företagsmiljöer där kunden betalar direkt, till exempel kontant, med PayPal eller kreditkort, kan du välja den relevanta metoden i fältet **Betalningssätt** på försäljningsfakturan. Betalningen bokförs sedan direkt på den bokförda fakturan. För betalningstjänster måste du även fylla i fältet **Betalningstjänst** fält. Mer information finns i [Aktivera kundbetalningar via betalningstjänster](sales-how-enable-payment-service-extensions.md).

Du kan även skapa direktbetalade fakturor för icke-registrerade kunder genom att definiera ett ”kontant” kundkort som du refererar till på försäljningsfakturan. Mer information finns i [Skapa kontantkunder](finance-how-to-set-up-cash-customers.md).  

Det är enkelt att korrigera eller annullera en bokförd försäljningsfaktura, innan den betalas. Det är användbart om du vill rätta till ett skrivfel eller om du kunden göra en ändring tidigt i orderprocessen. Mer information finns i [Så här kan du korrigera eller annullera obetalda försäljningsfakturor](sales-how-correct-cancel-sales-invoice.md). Om den bokförda försäljningsfakturan betalas, måste du skapa en försäljningskreditnota för att återföra försäljningen. Mer information finns i [Behandla försäljningsreturer eller annulleringar](sales-how-process-sales-returns-cancellations.md).

Artiklar kan vara både lagerartiklar och tjänster, betecknade med typerna **Lager** och **Tjänst** på artikelkortet. Försäljningsfakturaprocessen är samma för båda artikeltyper. Mer information finns i [Registrera nya artiklar](inventory-how-register-new-items.md).

Du kan fylla i kundfälten på försäljningsfakturan på två sätt, beroende på om kunden redan har registrerats. Se steg 2 och 3 i följande procedur.

## <a name="to-create-a-sales-invoice"></a>Så här skapar du en försäljningsfaktura
1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Försäljningsfakturor** och välj sedan relaterad länk.  
2. Ange namnet på en befintlig kund i fältet **Kund**.

   Andra fält i fönstret **Försäljningsfaktura** innehåller standardinformation om den valda kunden. Om kunden inte är registrerad, gör så här:
3. Ange namnet på en ny kund i fältet **Kund**.
4. Välj knappen **ja** i dialogrutan om registrering av den nya kunden.
5. Välj en mall det nya kundkortet ska baseras på i fönstret **Välj en mall för en ny kund** och välj sedan knappen **OK**.
6. Ett nytt kundkort visar information från den markerade kundmallen. Fyll i resterande fält. Mer information finns i [Registrera nya kunder](sales-how-register-new-customers.md).  
7. Välj **OK** för att gå tillbaka till fönstret **Förs.faktura**, när du har slutfört kundkortet.

   Flera fält i försäljningsfakturahuvudet är nu ifyllda med information som du har angett på det nya kundkortet.  
8. I fönstret **Inkommande dokument** fyller du i de återstående fälten efter behov. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

    Du är nu klar att fylla i försäljningsfakturaraderna för produkter som du säljer till kunden eller för en transaktion med den kund som du vill registrera en post i ett redovisningskonto.   

    Om du har ställt in återkommande försäljningsrader för kunden, till exempel en månatlig återanskaffningsorder, kan du infoga de här raderna på ordern, genom att välja åtgärden **Hämta återkommande försäljningsrader**.  
9. På snabbfliken **rader** i fältet **typ** väljer du vilken typ av produkt, kostnad eller transaktion som du vill bokföra för kunden med försäljningsraden.
10. I fältet **Nr.** väljer du en post som ska bokföras enligt värdet i fältet **typ**.

    Du lämnar fältet **Nr.** tomt i följande fall:

    * Om raden är avsedd för en kommentar. Skriv kommentaren i fältet **beskrivning**.
    * Om raden är avsedd för en ej lagerförd artikel. Välj åtgärden **markera ej lagerförda artiklar**. Mer information finns i [Arbeta med ej lagerförda artiklar](inventory-how-work-nonstock-items.md).

11. I fältet **antal** anger du hur många enheter av produkt, kostnad eller transaktion som registreras på raden för kunden.  

    > [!NOTE]  
    >   Om artikeln är av typen **Tjänst**, eller fältet **Typ** innehåller **Resurs**, är kvantiteten en tidsenhet, till exempel timmar, enligt fältet **Enhetskod** på raden.  

    Värdet i fältet **Radbelopp** beräknas som *enhetspris* x *antal*.  

    Pris- och radbeloppen visas med eller utan omsättningsskatt beroende på vad du valde i fältet **Priser inkl. moms** på kundkortet.  
12. Om du vill ge en rabatt kan du ange ett procenttal i fältet **radrabatt %**. Värdet i fältet **Radbelopp** uppdateras i enlighet därmed.  

    Om du har ställt in särskild artikelpriser på snabbfliken **Försäljningspriser och försäljningsradrabatter** på kund- eller artikelkortet uppdateras priset och beloppet på försäljningsraden automatiskt om de överenskomna prisvillkorna uppfylls. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).  
13. Upprepa moment 9 till 12 för varje produkt som du vill att sälja till kunden.  

    Summorna under raderna beräknas automatiskt när du skapar eller ändrar rader.  
14. I fältet **Fakturarabatt** anger du ett belopp som ska dras från värdet som visas i fältet **Totalt inkl. moms**.

    Om du har ställt in fakturarabatter för kunden, då infogas det angivna procentsatsvärdet automatiskt i fältet **Fakturarabatt %** om kriteriet uppfylls, och det relaterade beloppet infogas i fältet **Inv. Rabattbelopp exkl. moms**. Mer information finns i [Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md).  
15. När försäljningsfakturaraderna slutförda väljer du åtgärden **Bokföra och skicka**.  

Dialogrutan **Bokför och skicka bekräftelse** visar kundens standardmetod för mottagning av dokument. Du kan ändra utskicksmetoden genom att välja sökknappen för fältet **Skicka dokument till**. Mer information finns i [Skapa Dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md).

Relaterade artiklar och kundtransaktionerna skapas nu i systemet, och försäljningsfakturan matas ut som ett PDF-dokument. Försäljningsfakturan tas bort från listan över försäljningsfakturor och ersätts med ett nytt dokument i listan över bokförda försäljningsfakturor.

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Konfigurera försäljning](sales-setup-sales.md)  
[Lagersaldo](inventory-manage-inventory.md)  
[Skicka dokument som e-post](ui-how-send-documents-email.md)  
[Bulkfakturering från Microsoft Bookings i Business Central ](finance-bookings.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
