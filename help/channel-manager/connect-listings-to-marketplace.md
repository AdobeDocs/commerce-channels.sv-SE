---
title: Anslut listor till Walmart
description: 'Anslut listor för [!DNL Commerce] produkter till [!DNL Walmart Marketplace]för att börja sälja.'
feature: Sales Channels, Integration, Products, Tools and External Services
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: 8a1f95cdb8817cfcc6ffa96b584c66e680a1c282
workflow-type: tm+mt
source-wordcount: '1005'
ht-degree: 0%

---

# Anslut listor till Walmart

Precis som andra marknadsplatser tillåter [!DNL Walmart] tredjepartssäljare att lista objekt som säljs av andra.

- [!DNL Walmart Marketplace] använder produktidentifierare som UPC och GTIN för att matcha produkter med befintliga [!DNL Walmart Marketplace]-listor.

- För matchade produkter uppdateras Walmart Marketplace-listan med produkterbjudandet [!DNL Commerce] när du ansluter en produkt från [!DNL Channel Manager].

- Vanligtvis visas produkterbjudanden med de lägsta priserna först i listan [!DNL Walmart Marketplace], men andra faktorer som recensioner påverkar också placeringen.

## Matcha produkter

När du matchar produkter skickar Channel Manager produktdata till [!DNL Walmart Marketplace] för att söka efter befintliga listor med attributvärden som matchar det mappade [!DNL Commerce]-produktattributet. Matchningskriterierna bestäms av [attributmappningskonfigurationen](map-catalog-attributes.md) för din butikskanal.

Om en matchning hittas uppdateras den befintliga produktlistan så att ditt erbjudande läggs till.

### Förutsättningar

Innan du matchar produkter måste du kontrollera att produktkatalogattributvärdena uppfyller Walmart-kraven och konfigurera produktattributsinställningarna. Se [Mappa katalogattribut](map-catalog-attributes.md).

#### Välj och matcha produkter

1. Öppna en ansluten försäljningskanal.

1. I **[!UICONTROL Listings]** väljer du produkter som har statusen *[!UICONTROL Draft]* för matchning.

   ![Välj produkter från listor och skicka för matchning](assets/products-in-marketplace-sales-channel.png){width="500" zoomable="yes"}

1. Välj **[!UICONTROL Match Products]**.

   Ett meddelande anger antalet produkter som skickats för matchning.

   Statusen för de valda produkterna ändras till [!UICONTROL *Bearbetar*] tills matchningsåtgärden har slutförts. Det kan ta upp till 30 minuter för Walmart Marketplace att slutföra matchningsåtgärden.

### Kontrollera matchningsstatus

När matchningen är klar väljer du **[!UICONTROL Refresh products]** för att visa aktuell produktstatus. *Matcha* eller *Fel*.

- **[!UICONTROL Match]** anger att produkten matchades. Ditt produkterbjudande var kopplat till en befintlig Walmart Marketplace-lista. Om [Marketplace-arkivet inte är aktivt](walmart-requirements.md#walmart-marketplace-store-status) visas *[!UICONTROL Staged for Match]* i kolumnen *[!UICONTROL Status detail]*. Mellanlagrade produkter ansluts automatiskt när [!DNL Walmart Marketplace]-butiken aktiveras.

- **[!UICONTROL Error]** anger att matchningen misslyckades på grund av något av följande problem:

   - [!DNL Channel Manager] kunde inte skicka för matchning på grund av ett anslutningsproblem.

   - Ingen matchning hittades.

   - Matchning hittades, men det går inte att ansluta listan eftersom [!DNL Walmart Marketplace] returnerade en felkod. Information om problemet finns i **[!UICONTROL Error Description]**.

### Kontrollera lista vid Walmart

När du har matchat produkter granskar du den uppdaterade produktlistan och verifierar produktinformation, pris och lagerkvantitet från [[!UICONTROL Walmart Marketplace Seller Account Items]-kontrollpanelen ](https://seller.walmart.com/items-and-inventory/manage-items) för att granska den uppdaterade produkten.

### Felsöka produktmatchningsfel

Om produktmatchningsåtgärden misslyckas med ett fel visas felmeddelandet i kolumnen *[!UICONTROL Status detail]* i produktlistan för [!UICONTROL Channel Manager].

Vanliga fel som returneras är felaktigt formaterade produkt-ID-värden eller nödvändiga attribut saknas.

#### Korrigera produkt-ID-värden

| Typ | Beskrivning | Exempel |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, det tolvsiffriga talet inklusive kontrollsiffran. </br></br>Om din UPC har färre än 12 siffror, till exempel UPC-E med 8 siffror, lägger du till nollor för att uppfylla kravet. | Ändra från `45678912345` till `045678912345` |
| GTIN | GTIN-14, det 14-siffriga talet inklusive kontrollsiffran. </br></br>Om ditt GTIN innehåller färre än 14 siffror lägger du till inledande nollor </br> för att uppfylla kravet. | Ändra `456789123456` till `0045678912345` |
| EAN | GTIN-13, det 13-siffriga talet inklusive kontrollsiffran. </br></br>Om din EAN har färre än 13 siffror lägger du till inledande </br> nollor för att uppfylla kravet. | Ändra från `4567891234` till `0004567891234` |

Mer information om felkoder på Walmart Marketplace finns i hjälpen för [Walmart Seller](https://sellerhelp.walmart.com/s/guide?article=000005844).

## Överför nya produktlistor

För produkter som inte matchar på Walmart Marketplace använder du en valmart-produktkategorimall i Excel för att massöverföra produktlistor. Du fyller i Walmart-mallen med produktkatalogdata som exporterats från din [!DNL Commerce]-instans.

Om du vill se nya produktlistor kontrollerar du i produktkatalogen att de produkter du tänker sälja på Walmart Marketplace har de attribut som krävs för produktlistor på Walmart Marketplace.

**Walmart Marketplace listings-Attribut requirements**

| **Attribut** | **Kravnivå** |
|--------------------------|-----------------------|
| SKU | Obligatoriskt |
| Produktnamn | Obligatoriskt |
| Produkt-ID-typ | Obligatoriskt |
| Produkt-ID | Obligatoriskt |
| Varumärke | Obligatoriskt |
| Kort beskrivning | Obligatoriskt |
| Försäljningspris | Obligatoriskt |
| Platsbeskrivning | Obligatoriskt |
| URL för huvudbild | Obligatoriskt |
| Leveransvikt | Obligatoriskt |
| Viktiga funktioner | Rekommenderas |
| Modellnummer | Rekommenderas |
| Tillverkarens namn | Rekommenderas |
| Tillverkarens artikelnummer | Rekommenderas |
| Storlek | Rekommenderas |
| Färg | Rekommenderas |
| URL för huvudbild | Valfritt |
| URL för ytterligare bild | Valfritt |
| Tillverkare | Valfritt |

### Förutsättningar

- Kontrollera att du uppfyller [GåMart-kraven](walmart-requirements.md).

- I din [!DNL Commerce]-produktkatalog kontrollerar du att katalogkonfigurationen för de produkter som ska listas på Walmart Marketplace har alla nödvändiga attribut och uppfyller riktlinjerna för innehåll på Walmart Marketplace.

- Kontrollera att cron-jobbet körs för att slutföra exportåtgärden.

   - Information om lokala instanser finns i [Konfigurera och kör cron](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/configure-cron-jobs.html).

   - Mer information om molninfrastrukturen i Adobe finns i [Konfigurera cron-jobb](https://experienceleague.adobe.com/docs/commerce-cloud-service/user-guide/configure/app/properties/crons-property.html).

### Skapa produktdatafilen som ska överföras

1. Hämta en produktlistemall från Walmart Seller Center på ditt [Walmart Seller-konto](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - Välj **[!UICONTROL Add Items]** på sidan för produktkatalogobjekt. Välj sedan **[!UICONTROL Add items in bulk]**.

     ![Lägg till objekt i gruppalternativ i objektkonfigurationen Walmart Marketplace](assets/walmart-seller-account-add-items-bulk.png){width="600" zoomable="yes"}

   - Välj **[!UICONTROL Full Setup]** på hämtningssidan. Välj sedan en artikelkategori och hämta kategorimallen.

     ![Alternativet Hämta kategorimall i objektkonfigurationen Walmart Marketplace](assets/walmart-seller-account-full-setup-download.png){width="600" zoomable="yes"}

   - Kontrollera att mallen innehåller de obligatoriska och rekommenderade attributen för produktlistan.

1. I [!DNL Commerce]-administratören väljer du de produktdata som ska exporteras från din [!DNL Commerce]-plats i Adobe.

   - Välj [!UICONTROL **System** > Dataöverföring > **Exportera**] i Admin.

   - Välj [!UICONTROL **Produkter**] på sidan [!UICONTROL Export] i fältet [!UICONTROL Entity Type].

   - Konfigurera urvalskriterierna för export av produktdata i tabellen [!UICONTROL Entity Attributes].

     Använd filter för att välja och konfigurera attributvärden som gäller för de produktkategorier som du säljer in. Se till att du inkluderar de attribut som krävs och rekommenderas för Walmart. (Mer information finns i [Exportera data](https://experienceleague.adobe.com/docs/commerce-admin/systems/data-transfer/data-export.html) i användarhandboken för Adobe [!DNL Commerce] .)

     Om du vill utesluta ett attribut från exporten markerar du kryssrutan [!UICONTROL **Uteslut**] i början av raden.

1. Rulla till slutet av attributtabellen och välj [!UICONTROL **Fortsätt**] för att starta dataexporten.

   CSV-exportfilen bearbetas via en meddelandekö med hjälp av cron-jobb och sparas i `var/export/folder`. (Se [Hantera meddelandeköer](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/message-queues/manage-message-queues.html) i *Konfigurationshandboken*.)

1. Öppna Excel-mallen för produktkategorin Walmart Marketplace och använd Excel-makrofunktionerna för att sammanfoga exporterade produktdata med Excel-mallen.

1. Överför Excel-filen med exporterade produktdata.

   - Gå tillbaka till sidan för produktkatalogobjekt i [Walmart Seller Center](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   - Välj [!UICONTROL **Lägg till objekt** > **Lägg till objekt i grupp**].
   - Dra det färdiga kalkylbladet till avsnittet Överför.
   - Välj [!UICONTROL **Skicka**].
   - Välj [!UICONTROL  **aktivitetsfeed**] om du vill visa förloppet.

Fullständiga anvisningar finns i [Lägg till objekt i grupp med hjälp av den fullständiga artikelspecifikationen](https://sellerhelp.walmart.com/s/guide?article=000007680) i hjälpen för [!DNL *Walmart Seller*].
