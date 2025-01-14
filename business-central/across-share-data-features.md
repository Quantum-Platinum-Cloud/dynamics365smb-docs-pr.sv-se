---
title: Dela data
description: Lär dig mer om olika sätt att dela affärsdata från Business Central.
author: jswymer
ms.topic: conceptual
ms.workload: na
ms.search.keywords: null
ms.date: 09/21/2022
ms.author: jswymer
---
# <a name="sharing-business-data-from-business-central" />Dela affärsdata från Business Central

Samarbete mellan personer inom och utanför en organisation är en vital del av de flesta företag. I [!INCLUDE[prod_short](includes/prod_short.md)] finns flera funktioner för att dela affärsdata, till exempel en lista över poster, specifika poster eller dokument. <!--, with others&mdash;even those people who don't have a Business Central license in some cases.-->

Med alla dessa funktioner skyddas åtkomst till data av licensen och behörigheterna för Business Central.

## <a name="copying-a-link" />Kopiera en länk

![Stöds](media/check.png) Business Central Online ![Stöds](media/check.png) Business Central lokalt

På valfri sida kan du kopiera sidans URL och sedan klistra in och distribuera den i andra typer av media såsom e-post, Teams-chattar och textmeddelanden. Det enklaste sättet att kopiera en länk är att välja **Dela** > **Kopiera länk** längst upp på sidan. Ett annat sätt är att kopiera hela URL-adressen direkt från webbläsarens adressruta.

### <a name="modify-the-page-link" />Ändra sidlänken

När du har kopierat en länk kan du, innan du skickar den, ändra URL-adressen för att ändra vad som ska visas när sidan öppnas. Du kan till exempel lägga till filter eller ange ett annat företag.

Mer information finns i [URL till webbklient](/dynamics365/business-central/dev-itpro/developer/devenv-web-client-urls).

### <a name="about-filtered-lists" />Om filtrerade listor

Med filterrutan på list sidor kan du använda filter för att begränsa posterna som visas i listan. Om du använder åtgärden **Kopiera länk** eller kopierar URL-adressen från webbläsaren innehåller sidlänken inte filterändringarna. Användare som öppnar länken kommer att se hela samlingen. Sättet att behålla filtreringen på en länk till en samlingssida är att först spara den filtrerade sidan som en **Vy**. Öppna sedan vyn och kopiera länken därifrån.

Mer information finns i [Sortera, söka och filtrera](ui-enter-criteria-filters.md).

## <a name="sharing-to-teams" />Dela med Teams

![Stöds](media/check.png) Business Central Online ![Stöds inte](media/x-icon.png) Business Central lokalt

Direkt från de flesta samlings- och informations sidor kan du skicka en länk till sidan till personer, grupper eller kanaler. Dela t.ex. en länk till en filtrerad vy över posterna. Om du har installerat [!INCLUDE[prod_short](includes/prod_short.md)]-appen för Teams kommer länken automatiskt att expanderas till ett kompakt kort som du kan ta med i meddelandet. Mottagarna kan sedan markera länken eller kortet så att sidan öppnas i Business Central.

Mer information finns i [Dela poster och sidlänkar i Teams](across-working-with-teams.md).

## <a name="sharing-through-onedrive" />Dela via OneDrive

![Stöds](media/check.png) Business Central Online ![Stöds](media/check.png) Business Central lokalt

Med Business Central är det enkelt att lagra, hantera och dela filer med andra personer via OneDrive för företag. På de flesta sidor där det finns filer, t.ex. Rapportinkorgen eller filer som är bifogade till poster, finns åtgärderna **Öppna i OneDrive** och **Dela**. Bägge åtgärder sparar en kopia av en fil i OneDrive. I OneDrive kan du använda dess funktioner för delning och bidrag för filen. Skillnaden i åtgärder är att **Öppna i OneDrive** öppnar filen i OneDrive. **Dela** öppnar en sida och låter dig välja vem du vill dela filen med. Mottagare får ett e-postmeddelande om att de kan komma åt filen från din OneDrive.

Mer information finns i [Dela filer i OneDrive](across-share-onedrive.md).

## <a name="opening-in-excel" />Öppna i Excel

![Stöds](media/check.png) Business Central Online ![Stöds](media/check.png) Business Central lokalt

För listsidor och listor som är inbäddade på en sida kan du använda åtgärden **Öppna i Excel**. Med den här åtgärden exporteras listan över poster till en Excel-arbetsbok (.xlsx-fil) som du kan dela med andra. I arbetsboken kan du också använda funktionen Dela som ingår i Excel.

Mer information finns i [Visa och redigera i Excel](across-work-with-excel.md).

## <a name="sharing-rows-or-tables" />Dela rader eller tabeller

![Stöds](media/check.png) Business Central Online ![Stöds](media/check.png) Business Central lokalt

Du kan dela en eller flera poster i en lista. Välj bara kortkommandot <kbd>Ctrl</kbd>+<kbd>C</kbd> för att kopiera till Urklipp. Klistra sedan in det du kopierade i ett annat program genom att trycka <kbd>Ctrl</kbd>+<kbd>V</kbd>. Om du till exempel kopierar tre försäljningsorder som klistras in i ett e-postmeddelande visas orderna i en snyggt formaterad tabell.

Mer information finns i [Vanliga frågor och svar om Kopiera och klistra in](faq-copy-paste.yml).

## <a name="see-also" />Se även

[Business Central och OneDrive integration](across-onedrive-overview.md)  
[Hantera OneDrive integrering med Business Central](admin-onedrive-integration.md)  
[OneDrive Vanliga frågor och svar](admin-onedrive-faq.md)
