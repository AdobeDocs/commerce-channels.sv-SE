---
title: Lägg till produkter i kanalbutiken
description: Skapa produktsortiment för Marketplace-försäljning genom att lägga till produkter från katalogen i försäljningskanalen
source-git-commit: 905bedaf1eacdc45b2b7f222e7703e1f7b3dfd9c
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Lägg till produkter i kanalbutiken

Välj produkter från kanalhanteraren [!DNL Commerce] katalog för Walmart Marketplace-försäljning.

Om du vill synkronisera produkter till försäljningskanalen måste de valda produkterna ha följande attributkonfiguration:

- **[!UICONTROL Publish to Channel Manager]** attribut är aktiverat

- Minst ett produktattribut måste matcha ett av [obligatoriska Walmart Marketplace-attribut](map-product-attributes-for-matching.md)-GTIN, ISBN, ISSN, UPC, EAN

När du har sparat markeringar importerar kanalhanteraren produktdata till kanalen. Den här processen kan ta upp till 30 minuter.

## Lägg till produkter i försäljningskanalen

1. Öppna produktkatalogen som är kopplad till din Channel Manager-butik.

   Välj **Lägg till produkter**.

   ![Lägg till produkter i en ansluten kanal](assets/add-initial-products-to-connected-channel.png)

   Katalogen öppnas på en ny flik.

1. I katalogproduktrutnätet väljer du produkter att sälja på Walmart Marketplace.

   ![Skicka produkter till den anslutna kanalen](assets/select-products-from-catalog.png)

1. Aktivera **[!UICONTROL Publish to Channel Manager]** för de markerade objekten.

   - Från **[!UICONTROL Actions]**, markera **[!UICONTROL Update attributes]**.

   - Bläddra till **[!UICONTROL Publish to Channel Manager]** och aktivera det.

   - Kontrollera att produktattributen innehåller minst ett av de produktbeskrivningar som krävs.

   - Välj **[!UICONTROL Save]**.

   Ett bekräftelsemeddelande visas.

   ![Produktimport från katalog till bekräftelsemeddelande för försäljningskanal](assets/product-import-from-catalog-confirmation.png)

   Om meddelandet anger att uppdateringen är schemalagd använder du [kö:consumers:start](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] om du vill bearbeta uppdateringen direkt.

   ```bash
   $ bin/magento queue:consumers:start product_action_attribute.update
   ```

1. Återgå till den anslutna försäljningskanalen i [!DNL Channel Manager].

   Visa produkter från **[!UICONTROL Listings]**. Till att börja med finns produkterna i *Utkast* status. Välj [!UICONTROL Refresh products]** för att uppdatera tabellen.

   ![Produkter som importerats till en ansluten försäljningskanal](assets/products-in-marketplace-sales-channel.png)
