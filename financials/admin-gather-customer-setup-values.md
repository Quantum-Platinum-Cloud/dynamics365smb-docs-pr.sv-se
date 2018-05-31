---
title: "Samla in kundinställningsvärden | Microsoft Docs"
description: "Du använder frågeformuläret för konfiguration för att lättare kunna minska din implementeringsarbetsbörda, detta genom att effektivisera arbetet med att konfigurera det nya företaget. Du kan skapa frågeformuläret för konfiguration i Business Central och sedan leverera den sedan till kunden som en Excel- (.xls) eller XML-fil."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 03/07/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: cab3117811ccaca1aca985818a7c2145858beb97
ms.contentlocale: sv-se
ms.lasthandoff: 03/22/2018

---
# <a name="gather-customer-setup-values"></a>Samla in kundinställningsvärden
Du använder frågeformuläret för konfiguration för att lättare kunna minska din implementeringsarbetsbörda, detta genom att effektivisera arbetet med att konfigurera det nya företaget. Du kan skapa frågeformuläret för konfiguration i [!INCLUDE[d365fin](includes/d365fin_md.md)] och sedan leverera den till kunden som en .xls- eller XML-fil.  

Du kan ändra alla standardvärden i ett frågeformulär för att bättre matcha kundbehoven.  

> [!TIP]  
>  Läs mer om hur du definierar värdena i fälten för leveransplanering, [Skapa metodtips: leveransplanering](setup-best-practices-supply-planning.md).  

När kunden har slutfört frågeformuläret kan du importera filen till kundens nya [!INCLUDE[d365fin](includes/d365fin_md.md)]-företag. Du och din kund validerar svaren i frågeformuläret innan du kopplar dem till företaget.

## <a name="to-create-a-configuration-questionnaire"></a>Så här skapar du ett konfigurationsfrågeformulär
Du kan använda ett frågeformulär för att bestämma omfattningen och behoven av konfigurationen. Du kan skapa ett nytt frågeformulär, eller ändra ett befintligt frågeformulär, genom att lägga till nya fråga eller frågeområden.  

 Du kan bara skapa frågeformulär för tabeller av omställningstyp. Du kan till exempel använda verktyg för att ge information i följande fönster:  

-   Företagsinformation  
-   Anl.tillg.inställningar  
-   Redovisningsinställningar  
-   Lagerinställningar  
-   Monteringsinställningar
-   Produktionsinställningar  
-   Inköpsinställningar  
-   Marknadsföringsinställning  
-   Serviceinställningar  
-   Försäljningsinställningar  
-   Lagerstyrningsinställningar  

> [!NOTE]  
>  För att visa en fullständig list över inställningstabeller väljer du ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), öppnar **Inställningar** och väljer sedan relaterad länk. Använd flyttningsfunktioner för att bestämma omfattningen för flyttning av transaktion data. Mer information finns i [Migrera kunddata](admin-migrate-customer-data.md).  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Konfigurationsfrågeformulär** och välj sedan relaterad länk.  
2. Välj åtgärden **Ny**. Fönstret **Frågeformulär för inställningar** öppnas.  
3. Välj åtgärden **Frågeområden**. Fönstret **Frågeområden** öppnas.  
4. Välj åtgärden **Ny**. Fönstret **Konfig. frågeområden** öppnas.  
5. I fältet **Tabell-ID** väljer du ID på den tabell som du vill samla in information om. Fälten **Tabellnamn** fylls i automatiskt.  
6. Välj åtgärden **Uppdatera frågor**. Varje fält i tabellen läggs till det frågeformulär med ett frågetecken efter sin rubrik.

Du kan formulera om rubriken för att klargöra hur fråga ska besvaras. Om ett fält exempelvis kallas "Namn" kan du ändra det till att ange "Namn på <data being collected>." Du kan också ge vägledning i fältet **Referens**, inklusive en Webbadress till en sida med ytterligare information.  

Du kan även ta bort frågor som du inte vill inkludera i frågeformuläret.  

> [!NOTE]  
>  Fältet **Svarsalternativ** beskriver typen och formatet på svaret med data som är lämpliga. Fältet **Svar** innehåller användarinskickad information.  
>   
>  Vid behov, kan du också definiera standardsvar i fältet **Svar**. Dessa värden används som standard för anpassad installation. Personen som fyller i profilfrågeformuläret kan dock ändra och uppdatera svaret.  

## <a name="to-complete-the-configuration-questionnaire"></a>Så här slutför du konfigurationsfrågeformuläret
Du använder frågeformuläret för konfiguration för att strukturera och dokumentera en detaljerad diskussion om kundens specifika behov. Du kan också använda det för att samla inställningsdata från kunden för att konfigurera relevanta [!INCLUDE[d365fin](includes/d365fin_md.md)] inställningstabeller, t.ex redovisningen, lager och kunder.  

> [!NOTE]  
>  Du kan också skapa ett eget frågeformulär för konfiguration om så behövs.  

1. Öppna det företag som du vill slutföra frågeformuläret för.
2. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Konfigurationsfrågeformulär** och välj sedan relaterad länk.  
3. Välj frågeformuläret för företaget och välj sedan åtgärden **Exportera till Excel**, alternativt åtgärden **Exportera till XML**.
4. Låt kunden slutföra konfigurationsfrågeformuläret genom att ange svaren i Excel-arbetsboken. Det finns formulär för varje frågeområde som har skapats för frågeformuläret.   
5. Välj åtgärden **Importera från Excel** och välj .xlsx-filen med kundens svar.  
6. Välj åtgärden **Frågeområden** för att inleda processen med att validera och tillämpa svaren i konfigurationsfrågeformuläret.  

## <a name="to-complete-a-questionnaire-from-the-configuration-worksheet"></a>Så här kan du fylla i ett frågeformulär från konfigurationskalkylarket  
Följande process visar ett alternativt sätt att använda konfigurationsfrågeformulär. Vi förutsätter att konfigurationspaketet som du har fått innehåller frågeformulär.  

1. Öppna konfigurationskalkylarket när du har importerat ett konfigurationspaket.  
2. För varje tabell där det finns ett frågeområde väljer du åtgärden **Frågor**. Sidan med frågeformuläret öppnas.  
3. Svara på frågorna och välj sedan åtgärden **Koppla svar**.  
4. Välj **OK** för att stänga frågeformuläret.

## <a name="to-validate-the-configuration-questionnaire"></a>Så här validerar du konfigurationsfrågeformuläret
Det är viktigt att validera frågeformuläret för konfiguration innan du kopplar det mot [!INCLUDE[d365fin](includes/d365fin_md.md)]-formatet. Det är även en sätt att se till att dataformatering bevaras under import från Excel.  

En gemensam valideringsuppgift är att kontrollera att textsträngar inte anges i datumfälten. Denna granskningsprocess är nödvändig eftersom svarsformatet i frågeformuläret inte valideras automatiskt när du kör funktionen **Koppla svar**.  

> [!NOTE]  
>  Vanligtvis är validering av frågeformulär för konfiguration en manuell process. Men det finns kontroller för regionala formateringsinkonsekvenser. Dessutom kan det uppstå fel om strukturen på [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen inte motsvarar strukturen på flyttningsdatabasen.  

1. I fönstret **Konfigurationsfrågeformulär** markerar du relevant frågeformulär och väljer sedan åtgärden **Frågeområden**.  
2. Öppna relevant frågeområde.  
3. För varje fråga, verifiera att värdet i fältet **Svar** motsvarar format som tillhandahålls i fältet **Svarsalternativ**. Kontrollera till exempel att adressen för ett företag är i textformat.  
4. Om du hittar fel, kan du utföra felsökning och göra korrigeringar i Excel, genom att exportera frågeformuläret och sedan importera det på nytt. Du kan även korrigera fel direkt i [!INCLUDE[d365fin](includes/d365fin_md.md)] när du granskar svaren i fönstret **Konfig. frågeområde**.  
5. Upprepa dessa steg för varje frågeområde.  

När du har slutfört din validering är din data klar att kopplas till databasen.  

## <a name="to-apply-answers-from-the-configuration-questionnaire"></a>Så här kopplar du svar från konfigurationsfrågeformuläret
Efter att du har importerat och verifierat information från ett frågeformulär för konfiguration kan du överföra inställningsdatan till de motsvarande tabellerna i [!INCLUDE[d365fin](includes/d365fin_md.md)]-databasen.  

1. Välj ikonen ![Söka efter sida eller rapport](media/ui-search/search_small.png "Ikonen Söka efter sida eller rapport"), ange **Konfigurationsfrågeformulär** och välj sedan relaterad länk. Fönstret **Frågeformulär för inställningar** öppnas.  
2. Markera ett konfigurationsfrågeformulär i listan och välj sedan åtgärden **Redigera lista**.  
3. Du kan koppla svar på två sätt.  

- Om du vill koppla hela frågeformuläret väljer du åtgärden **Koppla svar**.  
- För att koppla svar enbart för ett visst **Frågeområde** väljer du åtgärden **Frågeområden**, väljer ett **Frågeområde** i listan och sedan åtgärden **Koppla svar**.  

### <a name="to-verify-that-answers-have-been-applied-successfully"></a>Så här kontrollerar du att svar har kopplats korrekt  
1. Kontrollera inställningsfönstren för olika huvudområden av [!INCLUDE[d365fin](includes/d365fin_md.md)]. För att hitta fönstret väljer du ikonen ![Sök efter sida eller rapport](media/ui-search/search_small.png "Ikonen Sök efter sida eller rapport"), anger namnet på inställningsfönstret och väljer sedan relaterad länk.  
2. Kontrollera att fältet har fyllts i med rätt data från de olika frågeområdena i frågeformuläret för konfiguration.  

Du har nu konfigurerat inställningen med kundens verksamhetsinformationen och regler.

## <a name="see-also"></a>Se även  
[Konfigurera ett företag med RapidStart Services](admin-set-up-a-company-with-rapidstart.md)  
[Administration](admin-setup-and-administration.md)
