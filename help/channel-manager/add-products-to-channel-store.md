---
title: Lägg till produkter i kanalhanteraren
description: 'Skapa produktsortiment för [!DNL Walmart Marketplace] försäljning genom att lägga till produkter från katalogen i den försäljningskanal som konfigurerats i Channel Manager.'
feature: Sales Channels, Merchandising, Products
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: 0087d60791cf00e4ed2bffe992447ee8e592fd9b
workflow-type: tm+mt
source-wordcount: '329'
ht-degree: 0%

---


# Lägg till produkter i [!DNL Channel Manager]

Om du vill lägga till produkter i försäljningskanalen [!DNL Walmart Marketplace] väljer du dem i produktkatalogen [!DNL Commerce] och importerar dem till [!DNL Channel Manager].
Importprocessen kan ta upp till 30 minuter eller mer beroende på hur många produkter du väljer.

## Förutsättning

**[Mappa katalogattribut](map-catalog-attributes.md)** - I konfigurationen [!DNL Channel Settings] mappar du minst ett attribut från produktkatalogen [!DNL Commerce] till någon av de Walmart-produktidentifierare som krävs --GTIN, ISBN, ISSN, UPC, EAN.

## Listkrav

[!DNL Commerce] produktlistor måste ha följande obligatoriska attributkonfiguration:

- Attributet **[!UICONTROL Connect to Channel Manager]** är aktiverat

- Ange giltiga värden för de obligatoriska Walmart-attributen.

   - Minst ett produktattribut som matchar en av de [!DNL Walmart Marketplace] produktidentifierare som krävs - GTIN, ISBN, ISSN, UPC, EAN.

   - Produktpriset har angetts till högst två decimaler, till exempel `9.99`

   - Produktvikt angiven till högst två decimaler, till exempel `1.25`

>[!TIP]
>
>Mer information om hur du optimerar listor för din försäljningskanal finns i [guiden Optimering av kvalitet på Walmart Marketplace](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Lägg till produkter

1. Välj **Lägg till produkter** från en ansluten försäljningskanalbutik för att öppna produktkatalogen.

   ![Lägg till produkter i säljkanalsbutiken](assets/add-initial-products-to-connected-channel.png){width="600" zoomable="yes"}

   Katalogen öppnas på en ny flik.

1. I katalogproduktrutnätet väljer du produkter att sälja på [!DNL Walmart Marketplace].

   ![Skicka produkter till säljkanalsbutiken](assets/select-products-from-catalog.png){width="600" zoomable="yes"}

1. Aktivera attributet **[!UICONTROL Connect to Channel Manager]** för de markerade objekten.

   - Välj **[!UICONTROL Update attributes]** från **[!UICONTROL Actions]**.

   - Bläddra till attributet **[!UICONTROL Connect to Channel Manager]** och aktivera det.

   - Kontrollera att produktattributen innehåller minst en av de [!DNL Walmart Product IDs] som krävs.

   - Välj **[!UICONTROL Save]**.

     Ett bekräftelsemeddelande visas.

     ![Produktimport från katalog till bekräftelsemeddelande för försäljningskanal](assets/product-import-from-catalog-confirmation.png){width="400"}

     Om meddelandet anger att uppdateringen är schemalagd använder du kommandot [`queue:consumers:start`](https://experienceleague.adobe.com/docs/commerce-operations/configuration-guide/cli/start-message-queues.html) [!DNL CLI] för att bearbeta uppdateringen direkt.

     ```bash
     $ bin/magento queue:consumers:start product_action_attribute.update
     ```

1. När importen har slutförts kontrollerar du de produkter som du har lagt till genom att gå tillbaka till [!DNL Channel Manager] och välja **[!UICONTROL Listings]**.

   Produkterna har till att börja med statusen *Utkast*. Välj **[!UICONTROL Refresh products]** om du vill uppdatera tabellen.

1. Uppdatera vyn så att de nya produkterna som lagts till i Channel Manager visas genom att välja statuskortet **[!UICONTROL Draft]**.

   ![Produkter som importerats till en ansluten försäljningskanal](assets/products-in-marketplace-sales-channel.png){width="400" zoomable="yes"}


