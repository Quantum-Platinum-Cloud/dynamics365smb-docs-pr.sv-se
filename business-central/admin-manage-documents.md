---
title: Hantera, ta bort eller komprimera dokument | Microsoft Docs
description: "Behåll historiska data eller ta bort dessa."
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 09/01/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 696100bfbcc987b1d684e7987e7fd43979813282
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="manage-documents"></a>Hantera dokument
En central roll, till exempel programadministratören, måste regelbundet hantera historiska dokument genom att ta bort eller komprimera dem.  

## <a name="delete-documents"></a>Ta bort dokument
I vissa fall kan det hända att du behöver ta bort fakturerade inköpsorder som inte raderats. I [!INCLUDE[d365fin](includes/d365fin_md.md)] kontrolleras att borttagna inköpsorder har fakturerats helt. Du kan inte ta bort order som inte har fakturerats och inlevererats helt.  

Returorder tas vanligtvis bort när de har fakturerats. När du bokför en faktura överförs den till fönstret **Bokförd inköpskreditnota**. Om du har markerat kryssrutan **Returutleverans i kreditnota** i fönstret **Inköpsinställningar** överförs fakturan till fönstret **Bokförd returutleverans**. Du kan ta bort dokumenten med hjälp av batch-jobbet **Ta bort faktrd inköpsret.order**. Innan du tar bort, kontrollerar batch-jobbet om inköpsreturorder är helt levererade eller fakturerade.  

Avropsorder tas inte bort när du har behandlat och fakturerat alla relaterade inköpsorder. Du kan ta bort avropsorder med batch-jobbet **Ta bort fakturerade avropsorder**.  

Fakturerade serviceorder tas vanligtvis bort när de har fakturerats helt. När en faktura bokförs skapas en motsvarande transaktion i fönstret **Bokförda servicefakturor**. Det bokförda dokumentet kan visas från fönstret **Bokförd servicefaktura**.  

Tjänsteordern tas inte bort automatiskt, men om det totala antalet i ordern inte har bokförts från själva serviceordern, utan från fönstret **Servicefaktura**, gäller följande. Då kan du behöva ta bort fakturerade order som inte har tagits bort. Du kan göra detta genom att köra batch-jobbet **Ta bort fakturerade serviceorder**.  

## <a name="see-also"></a>Se även  
[Administration](admin-setup-and-administration.md)  
