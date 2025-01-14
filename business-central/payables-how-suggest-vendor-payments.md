---
title: Föreslå batch-jobb för leverantörsbetalningar
description: Du kan ange leverantörsbetalningsinställningar för att få förslag till betalningar som förfaller snart eller där en rabatt kan erhållas.
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'vendor payment, creditor, debt, balance due, AP'
ms.search.form: 256
ms.date: 04/01/2021
ms.author: edupont
---
# <a name="suggest-vendor-payments" />Betalningsförslag för lev.

På sidan **Betalningsjournal** kan du använda batch-jobbet **Föreslå leverantörsbetalning** för att föreslå betalningsrader. Rader för saker som t. ex. betalningar som förfaller snart eller betalningar där en kassarabatt finns tillgänglig föreslås utifrån dina inställningar.

För att dra full nytta av betalningsförslagen, måste du prioritera leverantörerna. Mer information finns i [Så här prioriterar du leverantörer](purchasing-how-prioritize-vendors.md).  

> [!NOTE]  
> Leverantörsreskontratransaktioner som är **Stoppade** tas inte med i batch-jobbet.  

> [!IMPORTANT]  
>   Om du vill utnyttja kassarabatterna och har angett ett disponibelt belopp, används beloppet för:  
    * Prioritera förfallna leverantörstransaktioner först efter prioritet.   
    * Förfallna leverantörstransaktioner som inte prioriterats.  
    * Öppna leverantörstransaktioner som är berättigade till kassarabatter, ordnade efter leverantörsnummer.  

## <a name="to-use-the-suggest-vendor-payments-function" />Om du vill använda funktionen Betalningsförslag för lev.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Betalningsjournaler** och väljer sedan relaterad länk.  
2. Öppna den relevanta journalen och välj sedan åtgärden **Betalningsförslag för lev.**.  
3. Fyll i fälten om det behövs. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  
4. Välj **OK**.  

## <a name="to-insert-the-due-date-as-posting-date-on-payment-journal-lines" />Så här infogar du förfallodatum som bokföringsdatum på betalningsjournalrader

När du använder **Betalningsförslag för lev.**-batchjobbet för att skapa betalningsrader för leverantörer, kan du fylla två specialfält så att de genererade raderna använder förfallodatumet för att beräkna bokföringsdatumet. Dessa fält är **Beräkna bokföringsdatum från dokumentets förfallodatum** och **Dokumentets förfallodatum är förskjutet**.  

> [!IMPORTANT]  
>   Du kan inte använda fältet **Beräkna bokföringsdatum från dokumentets förfallodatum** tillsammans med fältet **Utnyttja kassarabatter** eller fältet **Summering per leverantör**. Om bokföringsdatumet baseras på förfallodatum, så kan vissa kassarabatter kanske inte beräknas korrekt eftersom bokföringsdatumet är efter kassarabattdatumet.  

Dessutom, om det beräknade bokföringsdatum inträffar tidigare flyttas bokföringsdatumet fram till arbetsdatumet, och en varning visas.  

Du kan även skapa betalningsrader manuellt genom att använda förfallodatum för att beräkna bokföringsdatum. När du har installerat leverantörsreskontratransaktioner kan du använda åtgärden **beräkna bokföringsdatum** för att uppdatera bokföringsdatumet på journalraden med förfallodatumet för relaterad inköpsfaktura. Mer information finns i [Så här kopplar du inköpstransaktioner manuellt](payables-how-apply-purchase-transactions-manually.md).  

> [!NOTE]  
>   Om inköpsfakturan har förfallit kommer bokföringsdatum att anges till arbetsdatumet, och teckensnittet på raden ändras till röd färg.  

## <a name="see-related-microsoft-trainingtrainingmodulessuggest-vendor-payments-dynamics-365-business-central" />Se relaterad [Microsoft utbildning](/training/modules/suggest-vendor-payments-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Hantera Leverantörsreskontra](payables-manage-payables.md)  
[Göra betalningar](payables-make-payments.md)  
[Arbeta med redovisningsjournaler](ui-work-general-journals.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
