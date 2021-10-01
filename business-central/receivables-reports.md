---
title: Kundreskontra, rapporter och analyser
description: Se vilka produktionsrapporter och analyser som är tillgängliga i standardversionen av Business Central så att du kan hålla reda på dina kundreskontra.
author: edupont04
ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords: reporting
ms.date: 07/13/2021
ms.author: edupont
ms.openlocfilehash: 76de1625ee71b666b01d6b2fef1efe5605d9a418
ms.sourcegitcommit: a486aa1760519c380b8cdc8fdf614bed306b65ea
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 07/13/2021
ms.locfileid: "6543375"
---
# <a name="accounts-receivable-reports-and-analytics-in-business-central"></a>Kundreskontrarapporter och analys i Business Central

För att hjälpa dig att hantera dina kundreskontra i [!INCLUDE [prod_short](includes/prod_short.md)] är standardrapporter och analyser inbyggda. Det överskrider traditionella rapporteringsbegränsningar för att hjälpa dig att effektivt utforma olika typer av rapporter.  

## <a name="reports"></a>Rapporter

I följande tabell beskrivs några av de viktigaste rapporterna inom kundreskontrarapportering.

| Rapportera | Objekt-ID | Beskrivning |
|--|--|--|
| **Kundfordringar – ålder** | 120 | Visar utestående belopp med kunder, uppdelade i tidsintervall för förfallen tid. Rapporten visar även en del av kundens saldo, som inte förfaller och kan visas med eller utan dokumentinformation för varje kund. Den här rapporten är huvudrapport för avstämning av kundreskontra till redovisning. Om du inte har tillåtit direkt bokföring på de konton som används i kund bokföringsmallen, är den här rapporten en specifikation av de belopp som finns i redovisningen. |
| **Kundkontoutdrag** | 1316 | Skapar ett kundutdrag för ett angivet tidsintervall. Det skickas vanligtvis till kunderna för att ge dem en översikt över utestående belopp och även som en betalningspåminnelse för att betala eventuella förfallna belopp. Du kan välja att visa förfallna belopp i en separat sektion. Du kan inkludera ett åldersspann liknande det som används i rapporten **Kundfordringar – ålder**. För åldersspannet anger du *30D*, som innebär 30 dagar, intervall av sådana as30, 60, 90 och 90+ dagar försenade, från slutdatumet eller *1M+CM* som kommer att vara aktuell månad i ett separat intervall och sedan månadsintervall för föregående månader. **Obs!** i kund listan finns det även en separat åtgärd, **schemalagda rapporter**. Det här alternativet filtrerar inte till den kund som du har valt. Det är samma rapport som används när du vill skicka utdrag till alla/fler-kunder. |
| **Kundreskontralista** | 121 | Visar de öppna kundreskontra transaktionerna fram till slutdatumet. Den här rapporten innehåller liknande innehåll som kund rapporten, men utan någon indikation om transaktionen är försenad. **Obs!** datumfiltret används på de detaljerade kundreskontra transaktionerna. Det innebär att om du har gjort en senare betalning än slutdatumet som har kopplats till fakturor inom datumintervallet, visas fakturorna i rapporten som de stängts av per slutdatum. |
| **Kund – råbalans** | 129 | Visar nettoförändringar för kunder under den period som anges i datum filtret samt nettoförändringen för räkenskapsåret innevarande år för det räkenskapsår som motsvarar perioden som valdes. Rapporten är grupperad efter kundbokföringsmallar och ger en annan vy av kund redovisningen än rapporten **Kundfordringar – ålder**. **Obs!** om du inte har angett någon bokföringsperiod, kommer systemet inte att veta vilket räkenskapsår som ska användas och visar antingen år till datum från det senaste räkenskapsåret som definierats eller så väljer du den period som eventuellt kan vara från början av ett år.|
| **Kunder – huvudbok** | 104 | Visar alla kundreskontra transaktioner i det angivna datumfiltret. Den här rapporten används i allmänhet för att kontrollera att alla transaktioner för en viss kund redovisas, eller andra interna kontroller i kundreskontran. |
| **Kund - betalningsinleverans** | 211 | Skapar en betalningsbetalning för varje kund reskontra transaktion av typen **betalning**. Om betalningen har kopplats till fakturor anges fakturorna. annars kommer det bara att ange betalningsbeloppet som borttaget. Den här rapporten används för att skicka till kunder som vill ha dokumentation för betalningsmottagning.|
| **Stäm av kund- och leverantörskonton** | 33 |Visar de redovisningstransaktioner som skapas när du bokför kund- och leverantörstransaktioner, som delas per redovisningskonto och bokföringsmallar. Den här rapporten används för att stämma av saldona på kund- och leverantörsreskontra till redovisningssaldon. |
| **Kundsaldo-enk. ålderssammandr.**| 109 |Det här är en äldre version av en åldersrapport för kundfordringar. Vi rekommenderar att du använder rapporten **Kundfordringar - ålder** istället. |
| **Försäljningsstatistik** |112  |[!INCLUDE [reports-sales-statistics](includes/reports-sales-statistics.md)]<br>Den här rapporten kan även användas i kundreskontra eftersom det är enklare att snabbt söka efter bokförda betalningar, rabatter och försäljning för en viss kund.|
|**Kundlista**|101| Visar olika typer av grundläggande information om kunderna, t.ex. kundens kundbokföringsmall, rabattgrupp, dröjsmålsränte- och betalningsinformation, säljare, standardvaluta och kreditlimit i din lokala valuta (BVA) samt kundens aktuella saldo (i BVA). Rapporten kan t.ex. användas för att underhålla informationen i tabellen Kund.|

## <a name="see-also"></a>Se även

[Analysera bokslut i Microsoft Excel](finance-analyze-excel.md)  
[Arbeta med dimensioner](finance-dimensions.md)  
[Hantera anläggningstillgångar](fa-manage.md)  
[Översikt över lokala funktioner](about-localization.md)  
[Revisorupplevelse i [!INCLUDE[prod_long](includes/prod_long.md)]](finance-accounting.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]