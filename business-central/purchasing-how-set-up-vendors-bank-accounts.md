---
title: Skapa bankkonton för leverantörer
description: 'Lära dig hur du kopplar bankkonton till leverantörskort i Business Central, t.ex. kontaktinformation, SWIFT- och IBAN-koder.'
author: rubenseishima
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 07/04/2022
ms.author: a-reishima
---
# <a name="set-up-vendor-bank-accounts" />Skapa bankkonton för leverantörer

Precis som du kan använda bankkontoinformation på [!INCLUDE [prod_short](includes/prod_short.md)] för att hålla reda på ditt företags banktransaktioner kan du också ställa in bankuppgifter för leverantörer. Leverantörens bankkontodata kan förenkla betalningar till leverantörer i kombination med [AMC Banking 365 Fundamentals tillägget](ui-extensions-amc-banking.md) eller funktionen [Exportera betalningar till en bankfil](finance-make-payments-with-bank-data-conversion-service-or-sepa-credit-transfer.md).

## <a name="add-or-edit-a-vendor-bank-account" />Lägga till eller redigera ett leverantörs bankkonto

[!INCLUDE [purchase-vendor-bank-account](includes/purchase-vendor-bank-account.md)]

> [!TIP]
> Du kan definiera ytterligare leverantörs bankkonton på list sidan för **Leverantör bankkontolista**.

## <a name="set-up-a-preferred-vendor-bank-account" />Skapa önskat bankkonton för leverantörer

Om en leverantör har ett eller flera bankkonton och du vill ställa in ett önskat alternativ för betalningsjournalraderna gör du så här:

1. Välj den ![Glödlampa som öppnar funktionen Berätta 1.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Leverantörer** och väljer sedan relaterad länk.
2. Öppna kortet för leverantören.
3. På snabbfliken **betalningar** väljer du standard leverantörs bank kontot i fältet **Föredragen bankkontokod**.

## <a name="see-related-microsoft-trainingtrainingmodulescash-management-dynamics-365-business-central" />Se relaterad [Microsoft utbildning](/training/modules/cash-management-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Ställa in inköp](purchasing-setup-purchasing.md)  
[Registrera nya leverantörer](purchasing-how-register-new-vendors.md)  
[Skapa bankkonton](bank-how-setup-bank-accounts.md)  
[Använda tillägget AMC Banking 365 Fundamentals](ui-extensions-amc-banking.md)  
[Skapa tjänsten Envestnet Yodlee Bank Feeds](bank-how-setup-bank-statement-service.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
