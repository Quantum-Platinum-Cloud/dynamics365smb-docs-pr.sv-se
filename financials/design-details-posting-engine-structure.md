---
title: "Designdetaljer - Bokföringsmotorstruktur | Microsoft Docs"
description: "Bokföringsgränssnittet och vissa andra funktioner i kodmodul 12 använder funktioner i bokföringsmotorn för att förbereda och infoga redovisningstransaktioner och momstransaktionsposter. Bokföringsmotorn är också ansvarig för att skapa en registrering av redovisningen."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: e5044183beeeaab5eb1269b17e60391a43a33f0c
ms.contentlocale: sv-se
ms.lasthandoff: 09/22/2017

---
# <a name="design-details-posting-engine-structure"></a>Designdetaljer: Bokföringsmotorstruktur
Bokföringsgränssnittet och vissa andra funktioner i kodmodul 12 använder funktioner i bokföringsmotorn för att förbereda och infoga redovisningstransaktioner och momstransaktionsposter. Bokföringsmotorn är också ansvarig för att skapa en registrering av redovisningen.  
  
 Funktionerna i följande tabell tillhandahåller ett standardramverk för att utforma bokföringsprocedurer (t.ex. Code, CustPostApplyCustledgEntry, VendPostApplyVendLedgEntry, UnapplyCustLedgEntry, UnapplyVendLedgEntry och Reverse) samt exklusiv åtkomst till tabell 17, redovisningstransaktion.  
  
|Routine|Description|  
|-------------|---------------------------------------|  
|StartPosting|Initierar bokföringsbufferten TempGLEntryBuf, låser redovisningstransaktions- och momstransaktionstabellerna och initierar bokföringsperiod, bokförd redovisningsjournal och valutakurser. Bör bara anropas en gång, sedan är NextEntryNo 0.|  
|ContinuePosting|Kontrollerar och bokför orealiserad moms för föregående transaktion, ökar NextTransactionNo och förbereder bokföringen av nästa rad.|  
|FinishPosting|Slutför bokföringen genom att infoga redovisningstransaktioner från den tillfälliga bufferten i databastabellen. Används alltid tillsammans med StartPosting. Söker efter inkonsekvenser.|  
|InitGLEntry|Används för att initiera en ny redovisningstransaktion för standardredovisningsjournalrader. Returnerar GLEntry som parameter.|  
|InitGLEntryVAT|Samma som InitGLEntry men tilldelar också Motkonto och SummarizeVAT.|  
|InitGLEntryVATCopy|Samma som InitGLEntryVAT men kopierar också bokföringsmalldata från momstransaktionen innan SummarizeVAT.|  
|InsertGLEntry|Den enda funktion som infogar redovisningstransaktionen i den globala TempGLEntryBuf-tabellen. Använd alltid den här funktionen för att infoga.|  
|CreateGLEntry|Utför InitGLEntry, tilldelar alt. valutabelopp och utför sedan InsertGLEntry. Ersätter flera rader av kod med ett enda funktionsanrop.|  
|CreateGLEntryBalAcc|Samma som CreateGLEntry men tilldelar också Motkontotyp och Motkonto.|  
|CreateGLEntryVAT|Samma som CreateGLEntry men med ytterligare bearbetning för bokföringsmallar och lagring i en tillfällig momsbuffert:<br /><br /> `GLEntry.CopyPostingGroupsFromDtldCVBuf(DtldCVLedgEntryBuf,GenJnlLine."Gen. Posting Type");`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryVATCollectAdj|Samma som CreateGLEntry men med ytterligare insamling av justeringar och lagring i en tillfällig momsbuffert:<br /><br /> `CollectAdjustment(AdjAmount,GLEntry.Amount,GLEntry."Additional-Currency Amount",OriginalDateSet);`<br /><br /> `InsertVATEntriesFromTemp(DtldCVLedgEntryBuf,GLEntry);`|  
|CreateGLEntryFromVATEntry|Samma som CreateGLEntry men kopierar även bokföringsmallar från momstransaktion.|  
  
## <a name="see-also"></a>Se även  
 [Designdetaljer: Bokföringsgränssnittsstruktur](design-details-posting-interface-structure.md)