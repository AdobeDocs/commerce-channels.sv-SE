---
title: Lägg till produkter i säljkanalsbutiken
description: Skapa produktsortiment för [!DNL Walmart Marketplace] försäljning genom att lägga till produkter från katalogen i försäljningskanalen
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: e3b12c9ce1ad4b5be17284e98956a773d7ccca24
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 0%

---


# Lägg till produkter i säljkanalsbutiken

Synkronisera produkter till [!DNL Walmart Marketplace] säljkanal, du väljer produkter i [!DNL Commerce] produktkatalog och importera dem till Channel Manager. De valda produkterna måste ha följande attributkonfiguration:

- **[!UICONTROL Publish to Channel Manager]** attribut är aktiverat

- Minst ett produktattribut måste matcha ett av [obligatoriskt [!DNL Walmart Marketplace] attributes](map-catalog-attributes.md)-GTIN, ISBN, ISSN, UPC, EAN

Processen att importera produkter från [!DNL Commerce] för Channel Manager kan ta upp till 30 minuter eller mer beroende på hur många produkter du väljer.

## Lägg till produkter

1. Välj **Lägg till produkter** för att öppna produktkatalogen.

   ![Lägg till produkter i säljkanalsbutiken](assets/add-initial-products-to-connected-channel.png)

   Katalogen öppnas på en ny flik.

1. Välj produkter att sälja på i katalogproduktrutnätet [!DNL Walmart Marketplace].

   ![Skicka produkter till säljkanalsbutiken](assets/select-products-from-catalog.png)

1. Aktivera **[!UICONTROL Publish to Channel Manager]** för de markerade objekten.

   - Från **[!UICONTROL Actions]**, markera **[!UICONTROL Update attributes]**.

   - Bläddra till **[!UICONTROL Publish to Channel Manager]** och aktivera det.

   - Kontrollera att produktattributen innehåller minst ett av de obligatoriska [!DNL Walmart Product IDs].

   - Välj **[!UICONTROL Save]**.

      Ett bekräftelsemeddelande visas.

      ![Produktimport från katalog till bekräftelsemeddelande för försäljningskanal](assets/product-import-from-catalog-confirmation.png)

      Om meddelandet anger att uppdateringen är schemalagd använder du [kö:consumers:start](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] om du vill bearbeta uppdateringen direkt.

      ```bash
      $ bin/magento queue:consumers:start product_action_attribute.update
      ```

1. När importen är klar kontrollerar du de produkter som du har lagt till genom att gå tillbaka till [!DNL Channel Manager] och markera **[!UICONTROL Listings]**.

   ![Produkter som importerats till en ansluten försäljningskanal](assets/products-in-marketplace-sales-channel.png)

   Till att börja med finns produkterna i *Utkast* status. Välj **[!UICONTROL Refresh products]** för att uppdatera tabellen.

