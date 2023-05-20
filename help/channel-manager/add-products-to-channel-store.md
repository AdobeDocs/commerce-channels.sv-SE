---
title: Lägg till produkter i kanalhanteraren
description: Skapa produktsortiment för [!DNL Walmart Marketplace] försäljning genom att lägga till produkter från katalogen i den försäljningskanal som konfigurerats i Channel Manager.'
exl-id: 00932df7-bdc7-42a1-b269-88dffcc918bc
source-git-commit: aeeaca20cb54528f77e457d54a194d6603c08654
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Lägg till produkter i [!DNL Channel Manager]

Lägga till produkter i [!DNL Walmart Marketplace] försäljningskanal, välj dem i [!DNL Commerce] produktkatalog och importera dem till [!DNL Channel Manager].
Importprocessen kan ta upp till 30 minuter eller mer beroende på hur många produkter du väljer.

## Förutsättning

**[Mappa katalogattribut](map-catalog-attributes.md)**—I [!DNL Channel Settings] konfiguration, mappa minst ett attribut från [!DNL Commerce] produktkatalog till någon av de Walmart-produktidentifierare som krävs - -GTIN, ISBN, ISSN, UPC, EAN.

## Listkrav

[!DNL Commerce] produktlistor måste ha följande obligatoriska attributkonfiguration:

- **[!UICONTROL Connect to Channel Manager]** attribut är aktiverat

- Ange giltiga värden för de obligatoriska Walmart-attributen.

   - Minst ett produktattribut som matchar ett av de obligatoriska [!DNL Walmart Marketplace] produktidentifierare - GTIN, ISBN, ISSN, UPC, EAN.

   - Produktpriset anges till högst två decimaler, till exempel `9.99`

   - Produktvikt angiven till högst två decimaler, till exempel `1.25`

>[!TIP]
>
>Mer information om hur du optimerar listor för din försäljningskanal finns i [Walmart Marketplace - guide för kvalitetsoptimering](https://marketplace.walmart.com/wp-content/uploads/2020/09/WMP_listing_quality_optimization_guide.pdf).

## Lägg till produkter

1. Välj **Lägg till produkter** för att öppna produktkatalogen.

   ![Lägg till produkter i säljkanalsbutiken](assets/add-initial-products-to-connected-channel.png)

   Katalogen öppnas på en ny flik.

1. Välj produkter att sälja på i katalogproduktrutnätet [!DNL Walmart Marketplace].

   ![Skicka produkter till säljkanalsbutiken](assets/select-products-from-catalog.png)

1. Aktivera **[!UICONTROL Connect to Channel Manager]** för de markerade objekten.

   - Från **[!UICONTROL Actions]**, markera **[!UICONTROL Update attributes]**.

   - Bläddra till **[!UICONTROL Connect to Channel Manager]** och aktivera det.

   - Kontrollera att produktattributen innehåller minst ett av de obligatoriska [!DNL Walmart Product IDs].

   - Välj **[!UICONTROL Save]**.

      Ett bekräftelsemeddelande visas.

      ![Produktimport från katalog till bekräftelsemeddelande för försäljningskanal](assets/product-import-from-catalog-confirmation.png)

      Om meddelandet anger att uppdateringen är schemalagd använder du [kö:consumers:start](https://devdocs.magento.com/guides/v2.4/config-guide/cli/config-cli-subcommands-queue.html) [!DNL CLI] om du vill bearbeta uppdateringen direkt.

      ```bash
      $ bin/magento queue:consumers:start product_action_attribute.update
      ```

1. När importen är klar kontrollerar du de produkter som du har lagt till genom att gå tillbaka till [!DNL Channel Manager] och markera **[!UICONTROL Listings]**.

   Till att börja med finns produkterna i *Utkast* status. Välj **[!UICONTROL Refresh products]** för att uppdatera tabellen.

1. Uppdatera vyn för att visa de nya produkterna som lagts till i Channel Manager genom att välja **[!UICONTROL Draft]** statuskort.

   ![Produkter som importerats till en ansluten försäljningskanal](assets/products-in-marketplace-sales-channel.png)


