---
title: Använd OCR för att göra PDF-dokument till E-fakturor
description: Beskriver hur du kan använda en OCR-tjänst för att omvandla inkommande PDF-filer eller bildfiler till elektroniska dokument.
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 'electronic document, e-invoice, incoming document, OCR, ecommerce, document exchange, import invoice'
ms.date: 06/14/2022
ms.author: edupont
---
# <a name="use-ocr-to-turn-pdf-and-image-files-into-electronic-documents" />Använda OCR för att omvandla PDF- och bildfiler till elektroniska dokument

Från PDF eller bildfiler som du får från dina handelspartner kan du låta en extern OCR-tjänst (Optical Character Recognition) skapa elektroniska dokument som du kan konvertera till dokumentposter i [!INCLUDE[prod_short](includes/prod_short.md)]. När du exempelvis tar emot en faktura i PDF-format från leverantören, kan du [skicka den till OCR-tjänsten från sidan](#to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page) **Inkommande dokument**.

Ett alternativ till att skicka filen från sidan **Inkommande dokument** är OCR-tjänsten har alternativet att [skicka filen till en dedikerad e-postadress](#to-send-a-pdf-or-image-file-to-the-ocr-service-by-email). När du sedan får tillbaka det elektroniska dokumentet skapas en relaterad inkommande dokumentpost automatiskt i [!INCLUDE[prod_short](includes/prod_short.md)].

Efter några sekunder skickar OCR-tjänsten den bearbetade filen till sidan **inkommande dokument**som en elektronisk dokument post som kan [konverteras till en inköps faktura för leverantören](#to-receive-the-resulting-electronic-document-from-the-ocr-service), försäljningsfaktura, kreditnota eller en journalpost.

Eftersom OCR baseras på optisk läsning är det troligt att OCR-tjänsten tolkar tecknen i dina PDF- eller bildfiler fel första gången dokument från till exempel en viss leverantör behandlas. Det går kanske inte tolka företagslogotypen som leverantörens namn eller summan på ett kvitto kan misstolkas på grund av layouten. Du kan undvika att dessa fel vidarebefordras genom att korrigera felen i en separat version av sidan **Inkommande dokument**. Sedan skickar du korrigeringarna tillbaka till OCR-webbtjänsten för att utbilda den till att tolka de specifika tecknen och fält korrekt nästa gång den behandlar ett PDF eller bilddokument för samma leverantör. Mer information finns i [Så här utbildar du OCR-tjänsten till att undvika fel](across-how-use-ocr-pdf-images-files.md#to-train-the-ocr-service-to-avoid-errors).

Trafiken av filer till och från OCR-tjänsten bearbetas av en dedikerad Jobbkötransaktion. Denna jobbkö skapas automatiskt när du aktiverar den externa OCR-tjänsteanslutningen. Mer information finns i [Skapa inkommande dokument](across-how-setup-income-documents.md).

> [!NOTE]
> OCR-funktionen tillhandahålls av externa providers. Välj ett servicepaket som passar din organisation och/eller ditt land/din region. Sök efter tjänster som är kompatibla med [!INCLUDE[prod_short](includes/prod_short.md)] och information om tillgängliga funktioner på [AppSource.microsoft.com](https://go.microsoft.com/fwlink/?linkid=2081646).

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-from-the-incoming-documents-page" />Så här skickar du en PDF- eller bildfil till OCR-tjänsten från sidan Inkommande dokument

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inkommande dokument** och väljer sedan relaterad länk.
2. Skapa en ny inkommande dokumentpost och bifoga filen. Mer information finns i [Så här skapar du inkommande dokumentposter](across-how-create-income-document-records.md).  
3. Markera sedan en eller flera rader på sidan **Inkommande dokument** och välj sedan åtgärden **Skicka till jobbkö**.

   Värdet i fältet **OCR-status** ändras till **Klar**. Bifogad PDF eller bildfil skickas till OCR-servicen av jobbkön enligt uppställningen, förutsatt att inga fel finns.
4. Markera alternativt en eller flera rader på sidan **Inkommande dokument** och välj sedan åtgärden **Skicka till OCR-tjänst** för att direkt skicka filer för bearbetning.

   Värdet i OCR-status fältet ändras till **OCR-status** ändras till **Skickat**, förutsatt att inga fel finns.

## <a name="to-send-a-pdf-or-image-file-to-the-ocr-service-by-email" />Så här skickar du en PDF eller bildfil till OCR-tjänstn via e-post

Vidarebefordra e-post till OCR-tjänstleverantören från ditt e-postprogram med PDF- eller bildfilen bifogad. Se OCR-tjänstleverantörens webbplats för information om e-postadress att skicka till.

Eftersom ingen inkommande dokumentpost finns för filen skapas en ny post automatiskt på sidan **Inkommande dokument** när du får det resulterande elektroniska dokumentet från OCR-tjänsten. Mer information finns i [Så här skapar du inkommande dokumentposter](across-how-create-income-document-records.md).

> [!NOTE]  
> Om du arbetar med en Tablet PC eller en telefon, kan du skicka filen till OCR-servicen, så snart som du har tagit ett foto av dokumentet, eller så kan du skapa ett inkommande dokument direkt. Mer information finns i [Skapa inkommande dokumentposter genom att ta ett foto](across-how-create-income-document-records.md#create-an-incoming-document-record-by-taking-a-photo).

## <a name="to-receive-the-resulting-electronic-document-from-the-ocr-service" />Så här tar du emot det resulterande elektroniska dokumentet från OCR-tjänsten

Elektroniska dokument, som skapas med OCR-tjänsten från PDF- eller bildfilen tas emot automatiskt på sidan **Inkommande dokument** jobbkötransaktionen som konfigureras när du aktiverar OCR-tjänsten.

Om du inte använder en jobbkö, eller om du vill ta emot ett färdigt OCR-dokument snabbare än per jobbköuppställningen, kan du välja åtgärden **Ta emot från OCR-tjänst**. Det kommer att få alla dokument som slutförs av OCR-tjänsten.

> [!NOTE]  
> Om OCR-tjänsten är inställd på att kräva manuell verifiering av bearbetade dokument, när fältet **OCR-status** innehåller **Avvaktar verifiering**. I så fall utför du följande steg för att logga in på OCR-tjänstwebbplatsen manuellt för att kontrollera ett OCR-dokument.

1. I fälter**OCR-status** väljer du hyperlinken**Avvaktar verifiering**.
2. På OCR-servicewebbplatsen loggar du in med hjälp av autentiseringsuppgifter på OCR-servicekontot. Mer information finns i [Så här skapar du en OCR-tjänst](across-how-setup-income-documents.md#to-set-up-an-ocr-service).

   Information för OCR-dokumentet visas med både källinnehållet av PDF- eller bildfilen och de resulterande OCR-fältvärdena.
3. Granska fältvärdena och redigera dem manuellt eller ange värden i fält som OCR-servicen har taggat som osäkra.
4. Välj **OK**. OCR-processen är klar och det resulterande elektroniska dokumentet skickas till inkommande dokument på sidan **inkommande dokument** i [!INCLUDE[prod_short](includes/prod_short.md)], enligt jobbköuppställningen.
5. Upprepa steg 2 till 4 för alla andra OCR-dokument som ska valideras.

Du kan nu fortsätta med att skapa dokumentposter för de inlevererade elektroniska dokumenten i [!INCLUDE[prod_short](includes/prod_short.md)], manuellt eller automatiskt. Mer information finns i nästa procedur: Du kan också [koppla den nya inkommande dokumentposten till det bokförda eller icke bokförda befintliga dokumentet](across-how-connect-disconnect-income-document-records.md) så att källfilen är lätt att komma åt från [!INCLUDE[prod_short](includes/prod_short.md)].

## <a name="to-create-a-purchase-invoice-from-an-electronic-document-received-from-the-ocr-service" />Så här skapar du en inköpsfaktura från ett elektroniskt dokument som har tagits emot från OCR-servicen

Efterföljande procedur beskriver hur du skapar en inköpsfakturatransaktion från en leverantörsfaktura som tas emot som ett elektroniskt dokument från OCR-servicen. Proceduren är samma när du skapar, till exempel, en redovisningsjournalrad från ett kostnadskvitto eller från en försäljningsreturorder.

> [!NOTE]  
> Fälten **Beskrivning** och **Nr.** på de nya dokumentraderna kommer endast att fyllas i om du först har mappat text som finns på OCR-dokumentet till de två fälten i [!INCLUDE[prod_short](includes/prod_short.md)]. Du kan göra den här mappningen som referenser till artikel, för dokumentrader av typartikel. Mer information finns i [Använd artikelreferenser](inventory-how-use-item-cross-refs.md). Du kan också använda **mappningsfunktionen Text-till-konto**. Mer information finns i avsnittet [Mappa ett inkommande dokument till en viss leverantör, redovisning eller adress](across-how-use-ocr-pdf-images-files.md#to-map-text-on-an-incoming-document-to-a-specific-vendor-account).

1. Markera raden för inkommande dokument och välj sedan åtgärden **skapa dokument**.

En inköpsfaktura kommer att skapas av [!INCLUDE[prod_short](includes/prod_short.md)] utifrån informationen i det elektroniska leverantördokumentet som du fick av OCR-servicen. Informationen infogas i den nya inköpsfakturan, baserat på mappningen som du har definierat som en referens eller mappningen text-till-konto.

Eventuella valideringsfel som vanligtvis beror på fel eller saknade data [!INCLUDE[prod_short](includes/prod_short.md)], visas på snabbfliken **Fel och varningar**. För mer information, se avsnittet [Så här hanterar du fel vid mottagning av elektroniska dokument](across-how-use-ocr-pdf-images-files.md#to-handle-errors-when-receiving-electronic-documents).

### <a name="to-map-text-on-an-incoming-document-to-a-specific-vendor-account" />Du mappar ett inkommande dokument till ett särskilt leverantörskonto

För inkommande dokument använder du vanligtvis åtgärden**Mappa text till konto** för att definiera att en viss text på en leverantörsfaktura som har tagits emot från OCR-servicen mappas till en viss leverantörskonto. Framöver innebär varje del av den inkommande dokumentbeskrivningen som finns som en mappningstext att **Leverantörsnummer** på resulterande dokument eller journalrader av typ *redovisningskonto* fylls med leverantören i fråga.

Förutom fördelning eller mappning till ett leverantörskonto eller redovisningskonton kan du också mappa text till ett bankkonto. Detta alternativ är användbart till exempel, för elektroniska dokument för kostnader som redan har betalats, där du vill skapa en redovisningsjournalrad som är klar för bokföring på ett bankkonto.

1. Välj relevant dokumentrad för inkommande och välj åtgärden **Mappa Text till kontot**. Sidan **Mappa text till konto** öppnas.
2. I fältet **Mappa text** anger du en text som förekommer på leverantörsfakturor som du vill skapa inköpsdokument eller journalrader för. Du kan ange upp till 50 tecken.
3. I fältet **Leverantörsnr** anger du den leverantör som det resulterande inköpsdokumentet eller journalraden skapas för.
4. I fältet **debetkontonr** anger du den typ av debetkonto som ska skrivas in på färdiga dokument- eller journalrader av typen Redovisningskonto.
5. I fältet **kreditkontonr** anger du den typ av kreditkonto som ska skrivas in på färdiga dokument- eller journalrader av typen Redovisningskonto.

   > [!NOTE]
   > Använd inte fälten **Ursprungstyp för motkonto** och **Ursprungsnr för motkonto** fält i samband med inkommande dokument. De används endast för automatisk betalningsavstämning. Mer information finns i [Mappa text på återkommande betalningar till konton för automatisk avstämning](receivables-how-map-text-recurring-payments-accounts-auto-reconcilliation.md).
6. Upprepa steg 2 till 5 för all text på inkommande dokument som du vill automatiskt vill skapa dokument för.

## <a name="to-handle-errors-when-receiving-electronic-documents" />Så här hanterar du fel vid mottagning av elektroniska dokument

1. På sidan **Inkommande dokument** välj raden för ett elektroniskt dokument som tagits emot från OCR-tjänsten med fel, indikerat av *Fel* i fältet **OCR-status**.
2. På sidan **Inkommande dokument** väljer du åtgärden **Redigera**.
3. På snabbfliken**Fel och varningar** väljer du meddelandet och väljer sedanåtgärden**Öppna relaterade poster**.
4. Sidan som visar om det finns fel eller saknade data, till exempel ett leverantörskort med ett saknat fältvärde, öppnas.
5. Rätta felet eller felen som beskrivs i varje felmeddelande.
6. Fortsätt med att bearbeta det inkommande dokumentet elektroniskt genom att välja åtgärden**Skapa manuellt** igen.
7. Upprepa steg 5 och 6 för alla återstående fel, tills det elektroniska dokumentet kan tas emot korrekt.

## <a name="to-train-the-ocr-service-to-avoid-errors" />Så här utbildar du OCR-tjänsten till att undvika fel

Eftersom OCR baseras på optisk läsning är det troligt att OCR-tjänsten tolkar tecknen i dina PDF- eller bildfiler fel första gången dokument från till exempel en viss leverantör behandlas. Det går kanske inte tolka företaglogotypen som leverantörens namn eller summan på ett utläggskvitto kan misstolkas på grund av layouten. Du kan undvika sådana fel genom att korrigera uppgifterna som du får av OCR-tjänsten och skicka återkopplingen till tjänsten.

Sidan **OCR-datakorrigering** som öppnas från sidan **Inkommande dokument** visar fälten från snabbfliken **Ekonomisk information** i två kolumner, en med ändringsbara OCR-uppgifter och en med skrivskyddade OCR-uppgifter. När du väljer knappen **Skicka OCR-feedback** skickas innehållet på sidan **OCR-datakorrigering** till OCR-tjänsten. Nästa gång tjänsten behandlar PDF- eller bildfiler som innehåller samma uppgifter tas dina korrigeringar med för att förbättra dokumentigenkänningen.

1. Välj den ![Glödlampa som öppnar funktionen Berätta.](media/ui-search/search_small.png "Berätta för mig vad du vill göra") anger du **Inkommande dokument** och väljer sedan relaterad länk.
2. Öppna en inkommande dokumentpost som innehåller data som har tagits emot från OCR-servicen och som du vill rätta till.
3. På sidan **Inkommande dokument** väljer du åtgärden **Korrigera OCR-data**.
4. Skriv över data i den redigerbara kolumnen för varje fält som har ett inkorrekt värde på sidan **OCR-datakorrigering**.
5. För att ångra korrigeringar som du har gjort sedan du öppnade sidan **OCR-datakorrigering** väljer du åtgärden **Återställ OCR-data**.
6. För att skicka korrigeringar till OCR-tjänsten väljer du åtgärden **Skicka OCR-feedback**.
7. Om du vill spara korrigeringarna stänger du sidan **OCR-datakorrigering**.

Fälten på snabbfliken **Ekonomisk information** på sidan **Inkommande dokument** uppdateras med alla nya värden som du har angett i steg 4.

## <a name="see-related-microsoft-trainingtrainingmodulesincoming-documents-dynamics-365-business-central" />Se relaterad [Microsoft utbildning](/training/modules/incoming-documents-dynamics-365-business-central/)

## <a name="see-also" />Se även

[Skapa inkommande dokument poster ](across-how-create-income-document-records.md)
[Skapa inkommande dokument poster direkt från dokument och poster](across-how-connect-disconnect-income-document-records.md)
[Iinkommande dokument](across-income-documents.md)  
[Inköp](purchasing-manage-purchasing.md)  
[Arbeta med [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  


[!INCLUDE[footer-include](includes/footer-banner.md)]
