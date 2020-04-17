---
title: Hantera alternativvärden som saknas
description: Lär dig mer om hur du förhindrar fullständig synkronisering från att misslyckas eftersom alternativen skiljer sig åt i mappade fält.
author: bholtorf
ms.author: bholtorf
ms.custom: na
ms.reviewer: na
ms.service: dynamics365-business-central
ms.topic: article
ms.date: 02/03/2020
ms.openlocfilehash: 42ad388e6c07ca259d4ef6095b9f8c908b509407
ms.sourcegitcommit: d67328e1992c9a754b14c7267ab11312c80c38dd
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 04/01/2020
ms.locfileid: "3196900"
---
# <a name="handling-missing-option-values"></a>Hantera alternativvärden som saknas
[!INCLUDE[d365fin](includes/cds_long_md.md)] innehåller bara tre alternativuppsättningsfält som innehåller alternati värden som du kan mappa till [!INCLUDE[d365fin](includes/d365fin_md.md)]-fält av alternativtyp<!-- Option type, not enum? @Onat can you vertify this? --> för automatisk synkronisering. Under synkroniseringen ignoreras icke-mappade alternativ, de saknade alternativen läggs till i relaterad [!INCLUDE[d365fin](includes/d365fin_md.md)]-tabellen och läggs till systemtabellen **CDS-alternativmappning** för att hanteras manuellt senare. Du kan t.ex. lägga till saknade alternativ i någon av produkterna och sedan uppdatera mappningen. I det här avsnittet beskrivs hur det fungerar.

Sidan **Tabellmappning för integrering** innehåller tre mappningar för fält som innehåller ett eller flera mappade alternativvärden. Efter en fullständig synkronisering innehåller sidan **CDSalternativmappning** de alternativ som inte är mappade i de tre fälten.

|         Transaktion             | Alternativvärde | Rubrik för alternativvärde |
|----------------------------|--------------|----------------------|
| Betalningsvillkor: 30 dagar netto       | 1            | 30 dagar netto               |
| Betalningsvillkor: 2%10 30 dagar netto   | 2            | 2% 10; 30 dagar netto        |
| Betalningsvillkor: 45 dagar netto       | 3            | 45 dagar netto               |
| Betalningsvillkor: 60 dagar netto       | 4            | 60 dagar netto               |
| Leveransmetod: FOB       | 1            | FOB                  |
| Leveransvillkor: DEBITERING  | 2            | Ingen avgift            |
| Speditör: FLYGFRAKT   | 1            | Flygfrakt             |
| Speditör: DHL        | 2            | DHL                  |
| Speditör: FEDEX      | 3            | FedEx                |
| Speditör: UPS        | 4            | UPS                  |
| Speditör: POSTALMAIL | 5            | Brev          |
| Speditör: FULLLOAD   | 6            | Full Load            |
| Speditör: WILLCALL   | 7            | Hämtas hos säljaren            |

Innehållet på sidan **Mappning av CDS-alternativ** baseras på uppräkningsvärden i tabellen **CDS-konto**. I [!INCLUDE[d365fin](includes/cds_long_md.md)] mappas följande fält på kontoeenheten till fält på transaktionerna för kund och leverantör:

- **Adress 1: leveransvillkor** för datatypen Enum (uppräkning), där värden definieras enligt följande:

```
enum 5335 "CDS Shipment Method Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "FOB") { Caption = 'FOB'; }
    value(2; "NoCharge") { Caption = 'No Charge'; }
}
```

- **Adress 1: leveranssätt** för datatypen Enum (uppräkning), där värden definieras enligt följande:

```
enum 5336 "CDS Shipping Agent Code"
enum 5336 "CDS Shipping Agent Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Airborne") { Caption = 'Airborne'; }
    value(2; "DHL") { Caption = 'DHL'; }
    value(3; "FedEx") { Caption = 'FedEx'; }
    value(4; "UPS") { Caption = 'UPS'; }
    value(5; "PostalMail") { Caption = 'Postal Mail'; }
    value(6; "FullLoad") { Caption = 'Full Load'; }
    value(7; "WillCall") { Caption = 'Will Call'; }
}
```

- **Betalningsvillkor** för datatypen Enum (uppräkning), där värden definieras enligt följande:

```
enum 5334 "CDS Payment Terms Code"
{
    Extensible = true;
    value(0; " ") { Caption = ' '; }
    value(1; "Net30") { Caption = 'Net 30'; }
    value(2; "2%10Net30") { Caption = '2% 10; Net 30'; }
    value(3; "Net45") { Caption = 'Net 45'; }
    value(4; "Net60") { Caption = 'Net 60'; }
}
```

Alla [!INCLUDE[d365fin](includes/d365fin_md.md)]-uppräkningar ovan mappas till alternativuppsättningar i [!INCLUDE[d365fin](includes/cds_long_md.md)].

### <a name="extending-option-sets-in-d365fin"></a>Utöka alternativuppsättningar i [!INCLUDE[d365fin](includes/d365fin_md.md)]
1. Skapa ett nytt AL-tillägg.

2. Lägg till ett Enum-tillägg för de alternativ som du vill utöka. Kontrollera att du använder samma värde. 

```
enumextension 50100 "CDS Payment Terms Code Extension" extends "CDS Payment Terms Code"
{
    value(779800001; "Cash Payment") { Caption = 'Cash Payment'; }
    value(779800002; "Transfer") { Caption = 'Transfer'; }
}
```

> [!IMPORTANT]  
> Du måste använda samma alternativ-ID-värden från [!INCLUDE[d365fin](includes/cds_long_md.md)] när du utökar [!INCLUDE[d365fin](includes/d365fin_md.md)]-uppräkningen. I annat fall misslyckas synkroniseringen.

> [!NOTE]
> De första tio tecknen i de nya alternativvärdenas namn och rubriker måste vara unika. Exempel: två alternativ med namnet "Överför 20 arbetsdagar" och "Överför 20 kalenderdagar" orsakar ett fel eftersom båda har samma första tio tecken, "Överföring 2". Namnge dem, till exempel "TRF20 WD" och "TRF20 CD".

### <a name="update-d365fin-option-mapping"></a>Uppdatera [!INCLUDE[d365fin](includes/cds_long_md.md)]-alternativmappningen
Du kan nu återskapa mappningen mellan [!INCLUDE[d365fin](includes/cds_long_md.md)]-alternativ och [!INCLUDE[d365fin](includes/d365fin_md.md)]-transaktioner.

På sidan **Mappning av integreringstabell** väljer du raden för **Betalningsvillkor** och väljer sedan åtgärden **Synkronisera ändrade transaktioner**. Sidan **Mappning för CDS-alternativ** uppdateras med ytterligare nedanstående transaktioner.

|         Transaktion                 | Alternativvärde   | Rubrik för alternativvärde |
|--------------------------------|----------------|----------------------|
| Betalningsvillkor: 30 dagar netto           | 1              | 30 dagar netto               |
| Betalningsvillkor: 2%10 30 dagar netto       | 2              | 2% 10; 30 dagar netto        |
| Betalningsvillkor: 45 dagar netto           | 3              | 45 dagar netto               |
| Betalningsvillkor: 60 dagar netto           | 4              | 60 dagar netto               | 
| **Betalningsvillkor: KONTANT**  | **779800001**  | **Kontant betalning**     |
| **Betalningsvillkor: ÖVERFÖRING**    | **779800002**  | **Överföring**         |

Tabellen **Betalningsvillkor** i [!INCLUDE[d365fin](includes/d365fin_md.md)] får då nya transaktioner för [!INCLUDE[d365fin](includes/cds_long_md.md)]-alternativen. I följande tabell visas nya alternativ i fetstil. Kursiva rader representerar alla alternativ som nu kan synkroniseras. Resterande rader representerar alternativ som inte används och kommer att ignoreras under synkroniseringen. Du kan ta bort dem eller utöka CDS-alternativen med samma namn.)

| Kod       | Formel för förfallodatum | Formel för rabattsdatum | Rabatt % | Beräkna kassarabatt i kr.nota | Beskrivning       |
|------------|----------------------|---------------------------|------------|-------------------------------|-------------------|
| 10 DAGAR    | 10D                  |                           | 0.         | FALSKT                         | 10 dagar netto       |
| 14 DAGAR    | 14D                  |                           | 0.         | FALSKT                         | 14 dagar netto       |
| 15 DAGAR    | 15D                  |                           | 0.         | FALSKT                         | 15 dagar netto       |
| 1M(8D)     | 1M                   | 8D                        | 2.         | FALSKT                         | 1 månad netto/2% 8 dagar |
| 2 DAGAR     | 2D                   |                           | 0.         | FALSKT                         | 2 dagar netto        |
| *2%10NET30* |                      |                           | 0.         | FALSKT                         |                   |
| 21 DAGAR    | 21D                  |                           | 0.         | FALSKT                         | 21 dagar netto       |
| 30 DAGAR    | 30D                  |                           | 0.         | FALSKT                         | 30 dagar netto       |
| 60 DAGAR    | 60D                  |                           | 0.         | FALSKT                         | 60 dagar netto       |
| 7 DAGAR     | 7D                   |                           | 0.         | FALSKT                         | 7 dagar netto        |
| ***KONTANT PAYME*** |                      |                           | 0.         | FALSKT                         |                   |
| AM         | AM                   |                           | 0.         | FALSKT                         | Aktuell månad     |
| PF        | 0D                   |                           | 0.         | FALSKT                         | Postförskott  |
| *NET30*      |                      |                           | 0.         | FALSKT                         |                   |
| *NET45*      |                      |                           | 0.         | FALSKT                         |                   |
| *NET60*      |                      |                           | 0.         | FALSKT                         |                   |
| ***ÖVERFÖRING*** |                      |                           | 0.         | FALSKT                         |                   |

## <a name="see-also"></a>Se även