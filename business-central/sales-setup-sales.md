---
title: "Översikt över proceduren för att konfigurera försäljningsprocesser | Microsoft Docs"
description: "Innehåller information om hur du definierar regler och värden för att definiera dina försäljningspolicyer och -processer."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: trade, sell, configure
ms.date: 10/26/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 00e83452109c6fa31c3eb56d5631f972e5239314
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="setting-up-sales"></a>Konfigurera försäljning
Innan du kan hantera försäljningsprocesser måste du konfigurera reglerna och värdena som definierar företagets försäljningspolicies.

Först måste du definiera allmänna inställningar, till exempel vilka försäljningsdokument som krävs och hur deras värden bokförs. Dessa allmänna inställningar görs vanligtvis bara en gång, under den initiala implementeringen.

En separat serie uppgifter relaterade till att registrera nya kunder är att registrera alla specialpriser eller rabattavtal som du har med varje kund.

Finansrelaterade försäljningar, till exempel betalningssätt och valutor, beskrivs i avsnittet Finans. Mer information finns i [Konfigurera ekonomi](finance-setup-finance.md).

| Om du vill | Gå till |
| --- | --- |
| Skapa ett kundkort för varje kund som du säljer till. |[Registrera nya kunder](sales-how-register-new-customers.md) |
| Låt kunder betala via PayPal, genom att välja PayPal-logotypen på försäljningsdokument. |[Så här aktiverar du kundutbetalning via PayPal](sales-how-enable-payment-service-extensions.md) |
| Ange olika rabatter och specialpriser som du beviljar kunden beroende på artikel, antal och/eller datum. |[Registrera försäljningspris, rabatt och betalningsavtal](sales-how-record-sales-price-discount-payment-agreements.md) |
| Skapa säljare så att du kan tilldela dem till kundkontakter eller mät säljares prestanda som grund för att beräkna deras försäljningprovision eller bonus. |[Skapa säljare](sales-how-setup-salespeople.md) |
| Ange hur försäljningsdokument ska skickas som standard för enskilda kunder eller för alla kunder när du väljer åtgärden **Bokför och skicka**. |[Skapa dokumentutskicksprofiler](sales-how-setup-document-send-profiles.md) |
| Konfigurera din e-post så att den innehåller en sammanfattning av informationen på försäljningsdokumentet som har skickats. |[Skicka dokument som e-post](ui-how-send-documents-email.md). |
|Du kan använda en EU-webbtjänst för att kontrollera kundens momsregistreringsnummer.|[Kontrollera momsregistreringsnummer](finance-setup-vat.md)|
|Ange information om de olika transportleverantörerna som du använder, bland annat en länk till deras godsupplysningstjänst.|[Så här konfigurerar du speditörer](sales-how-to-set-up-shipping-agents.md)|

## <a name="see-also"></a>Se även
[Försäljning](sales-manage-sales.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
