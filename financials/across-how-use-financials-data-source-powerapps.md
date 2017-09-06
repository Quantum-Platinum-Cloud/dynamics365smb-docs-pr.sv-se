---
title: "Använda din adata för att skapa en app | Microsoft Docs"
description: "Du kan göra dina Financials-data tillgängliga som datakälla och ange en OData-URL för dina webbtjänster för att skapa en företagsapp med PowerApps."
services: project-madeira
documentationcenter: 
author: edupont04
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: Odata, Power App, SOAP
ms.date: 06/02/2017
ms.author: edupont
ms.translationtype: Human Translation
ms.sourcegitcommit: 81636fc2e661bd9b07c54da1cd5d0d27e30d01a2
ms.openlocfilehash: e41a704d3a94abfb58d9547648f0eee46a8ed9b4
ms.contentlocale: sv-se
ms.lasthandoff: 07/07/2017


---
# <a name="connecting-to-your-financials-data-to-build-a-business-app-using-powerapps"></a>Ansluta till dina Financials-data och skapa en företagsapp med hjälp av PowerApps
Du kan göra din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data tillgänglig som underlag för datakälla i PowerApps.  

> [!NOTE]  
>   Du måste ha ett giltigt konto med [!INCLUDE[d365fin](includes/d365fin_md.md)] och med PowerApps.  

## <a name="to-add-included365finincludesd365finmdmd-as-a-data-source-in-powerapps"></a>Att lägga till [!INCLUDE[d365fin](includes/d365fin_md.md)] som datakälla i PowerApps.
1. I webbläsaren, går du till [powerapps.microsoft.com](https://powerapps.microsoft.com/en-us/), och loggar in.
2. Välj **Ny app** i den vänstra navigeringsrutan.
3. Välj redigerare, PowerApps Studio för Windows eller PowerApps Studio för webb.

   PowerApps Studio för Windows är ett program för att skapa och publicera PowerApps. PowerApps Studio för webb är en online-lösning som används för att skapa och publicera PowerApps.
4. Nästa steg för att skapa en PowerApp är att välja data. Välj pilikonen och välj sedan alternativet **ny anslutning** i det övre vänstra delen på sidan.
5. Välj i listan över tillgängliga anslutningar, välj **Dynamics 365 for Financials**.
6. PowerApps visar en anslutningssida som uppmanar dig till att ge den information som behövs för att ansluta till din [!INCLUDE[d365fin](includes/d365fin_md.md)]-data. Du måste ange en OData-URL, användarnamn, lösenord och företagsnamn för att ansluta.

   För den *OData-URL*, kan du kopiera OData V4-URL för någon av webbtjänsterna som finns på sidan **webbtjänster** i [!INCLUDE[d365fin](includes/d365fin_md.md)], som t.ex. `https://mycompany.financials.dynamics.com:7048/MS/ODataV4/`.  

   För *företagsnamn*, använder du namnet som visas i fältet **namn** i fönstret **företagsinformation** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Om din [!INCLUDE[d365fin](includes/d365fin_md.md)] innehåller flera företag, väljer du relevant företagsnamn i listan i fönstret **företag**. I båda fallen kontrollerar du att namnet som du anger i PowerApps-guiden motsvarar exakt den text som visas i [!INCLUDE[d365fin](includes/d365fin_md.md)], som t.ex. `My Company`.

   För användarnamn och lösenord, använder du de namn- och webbtjänstnycklar som har angetts för kontot i fönstret **användare** i [!INCLUDE[d365fin](includes/d365fin_md.md)]. Ditt användarnamn är till exempel *ADMIN* och webbtjänståtkomstnyckeln som fungerar som ditt lösenord och *EgzeUFQ9Uv0o5O0lUMyqCzo1ueUW9yRF3SsLU=*.
7. Klicka på knappen **Anslutning** för att fortsätta. PowerApps visar en standarddatauppsättning för [!INCLUDE[d365fin](includes/d365fin_md.md)]. Välj datauppsättningen **standard**.

   PowerApps visar en lista över tabeller som finns på [!INCLUDE[d365fin](includes/d365fin_md.md)]. Dessa listor eller slutpunkter motsvarar de webbtjänster som du har publicerat från ditt [!INCLUDE[d365fin](includes/d365fin_md.md)].

   Du kan också skapa en ny webbtjänst-URL i [!INCLUDE[d365fin](includes/d365fin_md.md)] med hjälp av åtgärden **skapa datauppsättning** på sidan **webbtjänster** med hjälp av den assisterade inställningsguiden **Ställ in rapportering**  eller genom att välja åtgärden **redigera i Excel** i någon lista.
8. Välj den tabell som du vill använda för din PowerApp och välj knappen **Anslut**.
9. Upprepa stegen för att lägga till ytterligare [!INCLUDE[d365fin](includes/d365fin_md.md)]-data till Power BI-datamodellen.

   > [!NOTE]  
>    När du har anslutit till [!INCLUDE[d365fin](includes/d365fin_md.md)], kommer du inte att uppmanas till att ge OData-URL, användarnamn och lösenord.

Nu har du lyckats ansluta till dina Dynamics 365-data och är redo att börja skapa din PowerApp. Mer information finns i [ PowerApp-dokumentation](https://powerapps.microsoft.com/tutorials/getting-started/).

## <a name="see-also"></a>Se även
[Välkommen till [!INCLUDE[d365fin_long](includes/d365fin_long_md.md)]](index.md)  
[Importera verksamhetsdata från andra finanssystem](upload-data.md)  
[Ställa in [!INCLUDE[d365fin](includes/d365fin_md.md)]](setup.md)  
[Ekonomi](finance.md)  
