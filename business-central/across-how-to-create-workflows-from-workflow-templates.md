---
title: "Så här skapar du arbetsflöden från arbetsflödesmallar | Microsoft Docs"
description: "Du kan spara tid när du skapar nya arbetsflöden genom att skapa arbetsflöden från arbetsflödesmallar."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 0f923c6d40093f35eb051e69ec149c3296bd0ee7
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="create-workflows-from-workflow-templates"></a>Skapa arbetsflöden från arbetsflödesmallar
Du kan spara tid när du skapar nya arbetsflöden genom att skapa arbetsflöden från arbetsflödesmallar.  

 Arbetsflödesmallar representerar icke-redigerbara arbetsflöden som finns i den generiska versionen av [!INCLUDE[d365fin](includes/d365fin_md.md)]. Koderna för arbetsflödesmallar som läggs till av Microsoft har prefixet ”MS-”.  

 Ett annat sätt att snabbt att skapa ett arbetsflöde är att importera ett befintligt arbetsflöde som du har i en fil utanför [!INCLUDE[d365fin](includes/d365fin_md.md)]. Mer information finns i [Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md).  

I fönstret **arbetsflöde** skapar du ett arbetsflöde genom att ange de berörda stegen på raderna. Varje steg består av en arbetsflödehändelse, modifierad av händelsevillkor, och ett arbetsflödesvar som modifieras av svarsalternativ. Du definierar arbetsflödesstegen genom att fylla i fält på arbetsflödesrader från fasta listor med händelse- och svarsvärden som representerar de scenarier som stöds av programkoden. Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).  

## <a name="to-create-a-workflow-from-workflow-template"></a>Så här skapar du ett arbetsflöde från en arbetsflödesmall  
1.  Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Söka efter sida eller rapport") gå till **Arbetsflöden** och välj sedan relaterad länk.  
2.  Välj åtgärden **skapa arbetsflödet från mallen**. Fönstret **arbetsflödesmallar**.  
3.  Markera en arbetsflödesmall och välj sedan knappen **OK**.  

     Fönstret **Arbetsflöde** öppnas för ett nytt arbetsflöde som innehåller all information för den valda mallen. Värdet i fältet **Kod** utökas med till exempel ”-01" för att ange att det är det första arbetsflödet som skapas från arbetsflödesmallen.  
4.  Fortsätt med att skapa arbetsflödet genom att redigera arbetsflödesstegen, eller lägg till nya steg. Mer information finns i [Skapa arbetsflöden](across-how-to-create-workflows.md).  

## <a name="see-also"></a>Se även  
 [Skapa arbetsflöden](across-how-to-create-workflows.md)   
 [Exportera och importera arbetsflöden](across-how-to-export-and-import-workflows.md)   
 [Visa arkiverade instanser för arbetsflödessteg](across-how-to-view-archived-workflow-step-instances.md)   
 [Ta bort arbetsflöden](across-how-to-delete-workflows.md)   
 [Genomgång: Konfigurera och använda ett arbetsflöde för godkännande av inköp](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Konfigurera arbetsflöden](across-set-up-workflows.md)   
 [Använda arbetsflöden](across-use-workflows.md)   
 [Arbetsflöde](across-workflow.md)   
