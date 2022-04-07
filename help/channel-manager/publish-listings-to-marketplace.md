---
title: Publicera listor till Walmart
description: Publicera listor för Commerce-produkter på Walmart Marketplace för att börja sälja.
exl-id: 78078b14-ebdd-415d-9486-66b0150167aa
source-git-commit: a10ab3f7fa7049e48d83a942f6c5441d8147b12c
workflow-type: tm+mt
source-wordcount: '1115'
ht-degree: 0%

---

# Publicera listor till Walmart

Precis som andra marknadsplatser tillåter Walmart tredjepartssäljare att lista artiklar som säljs av andra.

Plattformen använder produktidentifierare som UPC och GTIN för att matcha artiklar som redan är till salu.
För matchade produkter uppdateras den befintliga Walmart Marketplace-listan så att den omfattar erbjudandet om Commerce-produkt.

Vanligtvis visas produkter med de lägsta priserna i resultatet först, men andra faktorer som recensioner påverkar också placeringen.

## Matcha produkter

När du matchar produkter skickar Channel Manager produktdata till Walmart Marketplace för att söka efter befintliga listor med attributvärden som matchar det mappade Commerce-produktattributet. Matchningskriterierna bestäms av [konfiguration för attributmappning](map-product-attributes-for-matching.md) för er butikskanal.

Om en matchning hittas uppdateras den befintliga produktlistan så att ditt erbjudande läggs till.

### Förutsättningar

Innan du matchar produkter bör du kontrollera att produktkatalogattributvärdena uppfyller Walmart-kraven och konfigurera attributinställningarna. Se [Konfigurera produktmatchning](map-product-attributes-for-matching.md)

#### Välj och matcha produkter

1. Öppna en ansluten försäljningskanal.

1. Från **[!UICONTROL Listings]** väljer du produkter för matchning i *[!UICONTROL Draft]* status.

   ![Välj produkter från listor och skicka för matchning](assets/products-in-marketplace-sales-channel.png)

1. Välj **[!UICONTROL Match Products]**.

   Ett meddelande anger antalet produkter som skickats för matchning.

   ![Skicka produkter till den anslutna försäljningskanalen](assets/products-submit-for-matching.png)

   Status för valda produkter ändras till [!UICONTROL *Bearbetar*] tills matchningsåtgärden har slutförts. Det kan ta upp till 30 minuter för Walmart Marketplace att slutföra matchningsåtgärden.

### Kontrollera matchningsstatus

1. Välj **Uppdatera produkter** för att uppdatera den senaste produktstatusen.

1. Kontrollera produktstatus.

   När matchningen är klar kan statusen vara *Matcha* eller *Fel*.

   * **[!UICONTROL Match]** anger att produkten matchades. Ditt produkterbjudande publicerades i en befintlig Walmart Marketplace-lista.

   * **[!UICONTROL Error]** anger något av följande:

      * Ett fel uppstod och matchningsåtgärden misslyckades.

      * Ingen matchning hittades.

      * Matchningen hittades, men produkten publicerades som mellanlagrad eftersom [Marketplace-butiken är inte aktiv](walmart-prerequisites.md#walmart-marketplace-store-status).

### Kontrollera lista vid Walmart

Granska den uppdaterade produktlistan och verifiera produktinformation, pris och lagerkvantitet från [[!UICONTROL Walmart Marketplace Seller Account Items] kontrollpanel](https://seller.walmart.com/items-and-inventory/manage-items) för att granska den uppdaterade produkten.

### Felsöka produktmatchningsfel

Om produktmatchningen misslyckas returnerar Walmart Marketplace en felkod och i Channel Manager visas felstatusen i produktlistinformationen.

Visa felmeddelanden genom att hovra över **Fel** statusetikett. Vanliga fel som returneras är felaktigt formaterade produkt-ID-värden eller nödvändiga attribut saknas.

#### Korrigera produkt-ID-värden

| Typ | Beskrivning | Exempel |
|------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| UPC | GTIN-12, det tolvsiffriga talet inklusive kontrollsiffran. </br></br>Om din UPC har färre än 12 siffror, till exempel UPC-E med 8 siffror, lägger du till nollor för att uppfylla kraven. | Ändra från `45678912345` till `045678912345` |
| GTIN | GTIN-14, det 14-siffriga talet inklusive kontrollsiffran. </br></br>Om ditt GTIN innehåller färre än 14 siffror lägger du till inledande nollor </br>för att uppfylla kraven. | Ändra `456789123456` till `0045678912345` |
| EAN | GTIN-13, det 13-siffriga talet inklusive kontrollsiffran. </br></br>Om EAN har färre än 13 siffror lägger du till radavstånd </br>nollor för att uppfylla kravet. | Ändra från `4567891234` till `0004567891234` |

Mer information om felkoder på Walmart Marketplace finns i [Hjälp för Walmart Seller](https://sellerhelp.walmart.com/s/guide?article=000005844).

## Överför nya produktlistor

För produkter som inte matchar på Walmart Marketplace använder du en valmart-produktkategorimall i Excel för att massöverföra produktlistor. Du fyller i Walmart-mallen med produktkatalogdata som exporteras från din Commerce-instans.

Om du vill se nya produktlistor kontrollerar du i produktkatalogen att de produkter du tänker sälja på Walmart Marketplace har de attribut som krävs för produktlistor på Walmart Marketplace.

**Walmart Marketplace listings-Attributkrav**

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

* Verifiera att du uppfyller [Krav på genomgång](https://docs.google.com/document/d/1bEbCyVLXJQQsbZvEwetJvZKWQJOKoiw5Ia1uB4Bs4uo/edit#heading=h.k2lo9voad1gx).

* Kontrollera att katalogkonfigurationen för de produkter som ska listas på Walmart Marketplace har alla nödvändiga attribut i din Commerce-produktkatalog och uppfyller riktlinjerna för innehåll på Walmart Marketplace.

* Kontrollera att cron-jobbet körs för att slutföra exportåtgärden.

   * Information om lokala instanser finns i [Konfigurera och kör cron](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-cron.html).

   * Information om molninfrastrukturen i Adobe finns på [Ställ in cron-jobb](https://devdocs.magento.com/cloud/configure/setup-cron-jobs.html).

### Skapa produktdatafilen som ska överföras

1. Från [Walmart Seller-konto](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller)hämtar du en produktlistmall från Walmart Seller Center.

   * På sidan Produktkatalogobjekt väljer du **[!UICONTROL Add Items]**. Välj sedan **[!UICONTROL Add items in bulk]**.

      ![Lägg till objekt i grupp, alternativ i Objektkonfiguration på Walmart Marketplace](assets/walmart-seller-account-add-items-bulk.png)

   * På nedladdningssidan väljer du **[!UICONTROL Full Setup]**. Välj sedan en artikelkategori och hämta kategorimallen.

      ![Hämta kategorimallsalternativ i Objektkonfiguration på Walmart Marketplace](assets/walmart-seller-account-full-setup-download.png)

   * Kontrollera att mallen innehåller de obligatoriska och rekommenderade attributen för produktlistan.

1. Från [!DNL Commerce] Administratören väljer produktdata som ska exporteras från Adobe Commerce webbplats.

   * Välj [!UICONTROL **System** > Dataöverföring > **Exportera**].

   * På [!UICONTROL Export] sidan i [!UICONTROL Entity Type] fält, markera [!UICONTROL **Produkter**].

   * I [!UICONTROL Entity Attributes] konfigurera urvalskriterierna för export av produktdata.
   ![Exportera produktdatasidan i [!UICONTROL Commerce Admin]](assets/walmart-seller-account-full-setup-download.png)

   Använd filter för att välja och konfigurera attributvärden som gäller för de produktkategorier som du säljer in. Se till att du inkluderar de attribut som krävs och rekommenderas för Walmart (se [Exportera data](https://docs.magento.com/user-guide/system/data-export.html) i användarhandboken för Adobe Commerce för detaljerade anvisningar.)

   Om du vill utesluta ett attribut från exporten markerar du [!UICONTROL **Exkludera**] i början av raden.

1. Bläddra till slutet av attributtabellen och markera [!UICONTROL **Fortsätt**] för att starta dataexporten.

   CSV-exportfilen bearbetas via en meddelandekö med hjälp av cron-jobb och sparas i `var/export/folder`. (Se [Hantera meddelandeköer](https://devdocs.magento.com/guides/v2.4/config-guide/mq/manage-message-queues.html) i *Handbok för Commerce Developer*.)

1. Öppna Excel-mallen för produktkategorin Walmart Marketplace och använd Excel-makrofunktionerna för att sammanfoga exporterade produktdata med Excel-mallen.

1. Överför Excel-filen med exporterade produktdata.

   * Återgå till produktkatalogsobjektssidan i [Walmart Seller Center](https://login.account.wal-mart.com/authorize?responseType=code&amp;clientId=66620dfd-1f3f-479b-8b9c-e11f36c5438b&amp;scope=openId&amp;redirectUri=https://seller.walmart.com/resource/login/sso/torbit&amp;nonce=SX17QLMBKR&amp;state=ZBWWNZXXXM&amp;clientType=seller).

   * Välj [!UICONTROL **Lägg till objekt** > **Lägga till flera objekt samtidigt**].
   * Dra det färdiga kalkylbladet till avsnittet Överför.
   * Välj [!UICONTROL **Skicka**].
   * Välj [!UICONTROL  **Aktivitetsfeed**] för att visa förloppet.

Fullständiga anvisningar finns i [Lägg till objekt i grupp med hjälp av den fullständiga artikelspecifikationen](https://sellerhelp.walmart.com/s/guide?article=000007680) i [!DNL *Hjälp för Walmart Seller*].