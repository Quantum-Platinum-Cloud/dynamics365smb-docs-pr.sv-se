---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: c2f5f4c264150802920169139c90c0456f9a27c4
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334856"
---
I följande tabell beskrivs några av de viktigaste rapporterna inom leverantörsreskontrarapportering.

| Rapportera | Beskrivning | Id | 
|--|--|--|
| [Lev.skulder – ålder](https://businesscentral.dynamics.com?report=322) |Visar förfallna saldon för leverantörer i förfallna tidsintervall. Förfallna belopp kan visas som förfallo datum, bokföringsdatum eller efter dokumentdatum efter behov. Du kan välja att visa beloppen i lokal valuta (BVA) och skriva ut information om de förfallna dokumenten. Tidsintervallen kan ha rubriker med datum eller så är antalet förfallna i relation till den angivna åldern efter typ.<br>Den här rapporten är huvudrapport för avstämning av leverantörsreskontra till redovisning. Om du inte har tillåtit direkt bokföring på de konton som används i leverantörsbokföringsmallen för konto för kundreskontra, är den här rapporten en specifikation av de belopp som finns i redovisningen.| 322|
| [Leverantörsreskontralista](https://businesscentral.dynamics.com?report=321) | Visar leverantörens saldo per slutdatumet för angivet datumintervall. Du kan välja att visa leverantörssaldo i lokal valuta (BVA). Markera fältet **Ta bort borttagna transaktioner** för att visa de transaktioner som har stängts av slutdatumet, men som har avslutats (öppnats) vid ett senare datum. Markera **Visa transaktioner med noll saldo** om du vill visa leverantörer med saldon noll på datum filtrets slutdatum. Datum filtret gäller för de detaljerade leverantörsreskontratransaktionerna för transaktionerna i rapporten. Det innebär att om du har gjort en senare betalning än slutdatumet som har kopplats till fakturor inom datumintervallet, visas fakturorna i rapporten som de stängts av per slutdatum. | 321 |
| [Leverantörsråbalans](https://businesscentral.dynamics.com?report=329) | Visar nettoförändringar för leverantörer under den period som anges i datum filtret samt nettoförändringen för räkenskapsåret innevarande år för det räkenskapsår som motsvarar perioden som valdes. Rapporten är grupperad efter leverantörsbokföringsmallar och ger en annan vy av leverantörredovisningen än rapporten **Lev.skulder – ålder**. **Obs!** om du inte har angett någon bokföringsperiod, kommer systemet inte att veta vilket räkenskapsår som ska användas och visar antingen år till datum från det senaste räkenskapsåret som definierats eller så väljer du den period som eventuellt kan vara från början av ett år.|329 | 
| [Lev. – huvudbok](https://businesscentral.dynamics.com?report=304) | Visar alla leverantörsreskontratransaktioner i det angivna datumfiltret. Rapporten visar leverantörens ingående saldon i förhållande till datumfiltret. | 304 | 
| [Inköpsstatistik](https://businesscentral.dynamics.com?report=312) |[!INCLUDE [reports-purchase-statistics](reports-purchase-statistics.md)]<br>Den här rapporten kan även användas i leverantörsreskontra eftersom det är enklare att snabbt söka efter bokförda betalningar, rabatter och andra transaktioner för en viss leverantör.| 312 |
| [Lev.saldo – Ålderssammandrag](https://businesscentral.dynamics.com?report=305)| Äldre rapport för lev.skulder – ålder. Vi rekommenderar att du använder rapporten **Kundfordringar – ålder** istället. Du kan välja en period och ett datum som ska användas som *förfallet* per datum.|305| 
| [Stoppade betaln.](https://businesscentral.dynamics.com?report=319)| Visar leverantörs reskontra transaktioner där fältet **Stoppad** inte är tomt.| 319 |
| [Förskottsbetalningsjournal för leverantör](https://businesscentral.dynamics.com?report=317)|Visar utbetalningsjournal med information om kassarabatt och tolerans. Rapporten kan användas för att kontrollera betalningar innan betalningsfiler skapas och journalen bokförs. **Obs!** rapporten visar felaktigt kassarabatter när flera kreditnotor har använts i ett program. I det här fallet visas kassarabatten för de extra kreditnotorna som ett borttaget belopp.| 317 |
| [Leverantörslista](https://businesscentral.dynamics.com?report=301)|Visar olika typer av grundläggande information om leverantören, såsom leverantörsbokföringsmall, rabatt- och betalningsinformation, prioritetsnivå och leverantörens standardvaluta samt leverantörens aktuella saldo (i BVA). Rapporten kan t.ex. användas för att underhålla informationen i tabellen Leverantör.|301|