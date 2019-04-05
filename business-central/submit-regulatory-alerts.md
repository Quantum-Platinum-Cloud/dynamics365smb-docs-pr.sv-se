---
title: Skicka regelnotifieringar | Microsoft Docs
description: Du kan följa den här guiden om du vill skicka en andra varning till produktteamet om du vet om nya bestämmelser som kräver stöd för funktionen i Business Central.
author: sorenfriisalexandersen
ms.service: dynamics365-business-central
ms.topic: article
ms.reviewer: edupont
ms.search.keywords: ''
ms.date: 02/11/2019
ms.author: soalex
ms.openlocfilehash: a93e520bd5783e2c652242fbf0a01f0718e99b9c
ms.sourcegitcommit: 1bcfaa99ea302e6b84b8361ca02730b135557fc1
ms.translationtype: HT
ms.contentlocale: sv-SE
ms.lasthandoff: 03/08/2019
ms.locfileid: "808018"
---
# <a name="submit-alerts-about-countryregion-specific-regulatory-features"></a>Skicka notifieringar om lands-/regionspecifika regleringsfunktioner

Vi inbjuder dig till att använda Microsoft Dynamics Lifecycle Services (LCS) för att skicka regelnotifieringar Dynamics tjänst för att skicka regelnotifieringar.  

## <a name="to-submit-a-regulatory-alert-in-lcs"></a>Att skicka regelnotifiering i LCS

1. Gå till https://lcs.dynamics.com och logga in. Du visas de projekt som du har tillgång till

2. Markera projektet **regelnotifieringar - globala**. Detta öppnar projektet och visa olika saker som är relaterade till det här projektet

3. Markera **Notifieringstjänst** till höger i avsnittet **Fler verktyg**. Du visas en lista över meddelanden med rubriken **Dynamics skicka regelnotifieringar**

4. Du kan lägga till en ny notifiering genom att klicka på plustecknet **(+)** längst upp i listan. Detta ger dig en guide i 4 steg för att skapa notifieringen. Guiden har följande steg:
    - Sök efter befintliga objekt

        Sök efter all information som du tycker är relevant för notifieringen som du ska skapa. Om det inte finns några relevanta sökresultat kan du välja knappen **Skicka regelnotifiering** längst ned på sidan om du vill fortsätta med att skicka notifieringen.
    - Bifoga affärsprocesser

        Denna del gäller inte för Dynamics 365 Business Central. Välj **hoppa över** för att gå vidare till nästa steg.
    - Beskriv notifieringen

        Ange information om notifieringen i lämpligt fält. Obligatoriska fält är markerade med en röd asterisk (\*) i guiden.

        |Fält        |Description                               |
        |-------------|------------------------------------------|
        |Titel  | Ange en beskrivande rubrik för att identifiera berört område. Till exempel anger du *Ändringar i dokument från och med 1 juli 2019*. |
        |Description  | Ange en kort översikt över lagstiftningen. Beskrivningen bör fokusera på frågor som är relevanta för resursplanering inom företag (ERP), så att användare kan förstå kraven på en hög nivå utan att behöva läsa lagstiftningen först.|
        |Land  | Ange landet/regionen som lagstiftningen gäller för.|
        |Bransch| Ange vilken bransch om kravet bara gäller för specifika branscher. Välj till exempel **Offentliga sektorn**, **Butik** eller **Produktion**.|
        |Funktionsreferens  | Detta gäller inte för Dynamics 365 Business Central, men du kan ange en referens till en funktion om du känner till den. Listan med funktioner för ett visst land finns i [lokaliseringsportalen](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC). |
        |Datum för tillämpning av lagen  | Ange det datum då berörda kunder måste börja följa lagen.|
        |Datum när myndigheten tillkännagav meddelandet  | Ange det datum då myndigheten meddelade ändringen.|
        |Senaste arkiveringsdatum  | Välj deadline för den första överföringen av nya eller ändrade rapporten.|
        |Länka till lagstiftning  | Ange en eller flera länkar till offentliggjorda lagar, tolkningsriktlinjer, genomföranderiktlinjer eller annan användbar dokumentation som hjälper användare att förstå och implementera kraven.|
        |Företagsnamn  | Ange namnet på företaget för den person som skickar meddelandet.|
        |Kontaktnamn  | Ange namnet på den person som skickar meddelandet. |
        |E-postkontakt  | E-postadressen på den person som skickar meddelandet.|
        |Affärsprocess  | De affärsprocesser som du har valt via guiden **skicka notifiering**|
        |Kommentarer  | Ange eventuell ytterligare information som kan hjälpa användare att förstå och implementera kraven. Klicka på **Skicka** om du vill spara kommentarerna. Flera kommentarer kan läggas till och ska skickas separat. Kommentarer sparas i den ordning de har lagts till. |
        |Jag vill se ...  | Klicka på knappen **överför** och bläddra för att välja en fil som ska läggas till som bilaga. När du har markerat filen överförs och visas den som en länkad fil. Du kan lägga till upp till tre filer med storleken 5 MB var. För att ta bort filer som har bifogats klickar du på **Ta bort** under rubriken på filen. Bilagor måste vara allmänt tillgängligt material. De får inte vara ägda eller kundspecifika/partnerspecifika.|

        Klicka på **skicka** för att spara och skicka meddelandet.

        Om du inte har all information som krävs, eller om du inte är redo att skicka meddelandet, kan du spara en delvis slutförd notifiering.

    - Inlämningsbekräftelse

      När du har skickat meddelandet får du en bekräftelse på att meddelandet har skickats till Microsoft.

## <a name="see-also"></a>Se även

[Välkommen till Business Central](index.md)  
[Komma igång](product-get-started.md)  

## [!INCLUDE[d365fin](includes/free_trial_md.md)]  