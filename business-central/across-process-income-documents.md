---
title: Bearbeta Inkommande dokument | Microsoft Docs
description: "Om du vill registrera ett externt dokument, t.ex. en PDF i Business Central, måste du först skapa eller slutföra en inkommande dokumentpost."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice
ms.date: 06/02/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: b6de34be2f16cf0b9130bc88495f27536a9d5080
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="processing-incoming-documents"></a>Bearbeta inkommande dokument
Om du vill registrera ett externt dokument i [!INCLUDE[d365fin](includes/d365fin_md.md)], måste du först skapa eller slutföra en inkommande dokumentpost. Du kan göra detta manuellt eller så kan du ta ett foto på det externa dokumentet och sedan skapa en inkommande dokumentpost med bildfilen bifogad.

Från PDF eller bildfiler som du får från dina handelspartner kan du låta en extern OCR-tjänst (Optical Character Recognition) skapa elektroniska dokument som du kan konvertera till dokumentposter i [!INCLUDE[d365fin](includes/d365fin_md.md)]. När du exempelvis tar emot en faktura i PDF-format från leverantören, kan du skicka den till OCR-tjänsten från fönstret **Inkommande dokument**. Du kan också skicka filen till OCR-tjänsten via e-post. När du sedan får tillbaka det elektroniska dokumentet skapas en relaterad inkommande dokumentpost automatiskt. Efter några sekunder får du tillbaka filen från OCR-tjänsten som en elektronisk faktura som kan omvandlas till en inköpsfaktura för leverantören.

| Om du vill | Gå till |
| --- | --- |
| Skapa inkommande dokumentposter manuellt eller automatiskt, genom att ta ett foto av t.ex. ett papperskvitto. |[Skapa inkommande dokumentposter](across-how-create-income-document-records.md) |
| Använd en OCR-tjänst för att göra PDF- och bildfiler till elektroniska dokument, som t.ex. kan omvandlas till inköpsfakturor i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Utbilda OCR-tjänsten för att undvika fel nästa gång som den bearbetar liknande information. |[Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument](across-how-use-ocr-pdf-images-files.md) |
| Koppla eller ta bort inkommande dokumentposter för ett icke bokfört försäljnings- eller inköpsdokument och till en kund, leverantör eller redovisningstransaktion från dokumentet eller posten. |[Skapa inkommande dokumentposter direkt från dokument och transaktioner](across-how-connect-disconnect-income-document-records.md) |
| Från fönstren **Kontoplan** och **Redovisningstransaktioner** kan du använda en sökfunktion för att hitta redovisningsposter för bokförda dokument som inte har inkommande dokumentposter, och sedan länka dem till centralt befintliga poster eller skapa nya med bifogade dokumentfiler. |[Söka efter bokförda dokument utan inkommande dokumentposter](across-how-find-posted-documents-without-income-document-records.md) |
| Få en bättre översikt genom att ange inkommande dokumentposter som Bearbetade för att ta bort dem från standardvyn. |[Hantera många inkommande dokumentposter](across-how-manage-many-income-document-records.md) |

## <a name="see-also"></a>Se även
[Inkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
