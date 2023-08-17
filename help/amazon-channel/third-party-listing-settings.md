---
title: AMAZON SALES CHANNEL - [!UICONTROL Third-party Listings]
description: Uppdatera inställningarna för tredjepartslistan avgör om din Commerce-katalog importerar produkter från dina befintliga Amazon Seller Central-listor.
feature: Sales Channels, Products
exl-id: bc82775a-6f29-49b5-a80b-20e171eaf8f4
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# [!UICONTROL Third-party Listings]

Inställningarna för tredjepartslistan ingår i inställningarna för din butikslista. Du kommer åt listinställningarna via [instrumentpanel för butik](./amazon-store-dashboard.md).

Dessa inställningar avgör om [!DNL Commerce] kataloger importerar produkter från din befintliga [!DNL Amazon Seller Central] listor. Du bör importera listor från Amazon för att se till att alla listor matchar [!DNL Commerce] produkter. När dina listor ingår i [!DNL Commerce] kan du hantera alla produkter från en och samma katalog och använda funktionerna i Amazon försäljningskanal. Bland dessa funktioner märks orderhantering med Amazon, intelligent prissättning och kvantitetshantering.

När du har konfigurerat den för att importera dina Amazon-listor importerar Amazon försäljningskanal dina Amazon-listor till din [!DNL Commerce] katalog, försöker matcha dem med befintliga produkter. Om ingen matchning hittas automatiskt kan du importera Amazon-listan som en ny [!DNL Commerce] produkten eller manuellt matcha listningen mot en produkt.

Om du vill importera dina Amazon-listor väljer du [!DNL Commerce] för Amazon Seller SKU och Amazon ASIN. Om du inte har [!DNL Commerce] [produktattribut](./ob-creating-magento-attributes.md)kan du skapa och tilldela dem. Genom att mappa dessa attribut kan du matcha importerade Amazon-listor korrekt med dina [!DNL Commerce] produkter.

Den inledande listimporten startar när [butiksintegrering](./store-integration.md) är klar. Efteråt och baserat på dina kroninställningar [!DNL Commerce] söker kontinuerligt efter nya Amazon-listor (som inte har skapats i Amazon Sales Channel) och uppdaterar [!DNL Commerce] katalogen enligt inställningarna för tredjepartslistor.

## Konfigurera inställningar för tredjepartslistor

1. Klicka **[!UICONTROL Listing Settings]** på butikens kontrollpanel.

1. Expandera avsnittet _[!UICONTROL Third Party Listings]_.

1. För **[!UICONTROL Import Third Party Listings]** (obligatoriskt) väljer du ett alternativ:

   - `Import Listing` - (Standard) Välj när du vill att produktinformation från dina Amazon-listor ska importeras till [!DNL Commerce] produktkatalog. Det här alternativet är standard och rekommenderas.

   - `Do Not Import Listing` - Välj när du vill manuellt [skapa och tilldela nya produkter](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) till [!DNL Commerce] katalog för dina Amazon-listor.

   >[!NOTE]
   >Följande alternativfält är bara aktiva när de är inställda på `Import Listing`.

1. För **[!UICONTROL Attribute That Contains Amazon Seller SKU]** väljer du [!DNL Commerce] som matchar Amazon Seller SKU-värdet.

1. För **[!UICONTROL Attribute That Contains Amazon ASIN]** väljer du [!DNL Commerce] som du skapade och matchade det med Amazon ASIN.

   >[!NOTE]
   >Om du inte skapade dessa [!DNL Commerce] attribut för dina Amazon-listor finns i [Skapa attribut för Amazon Matching](./ob-creating-magento-attributes.md).

1. När du är klar klickar du på **[!UICONTROL Save listing settings]**.

![Tredjepartslistor](assets/amazon-third-party-listings.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|--------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Import Third Party Listings] | Obligatoriskt. Alternativ:<ul><li>**[!UICONTROL Import Listing]** - (Standard) Välj när du vill att produktinformation från dina Amazon-listor ska importeras till [!DNL Commerce] produktkatalog. </li><li>**[!UICONTROL Do Not Import Listing]** - Välj när du vill manuellt [skapa och tilldela nya produkter](https://experienceleague.adobe.com/docs/commerce-admin/catalog/products/products-list.html) till [!DNL Commerce] katalog för dina Amazon-listor.</li></ul> |
| [!UICONTROL Attribute That Contains Amazon Seller SKU] | Endast aktiv när den är inställd på `Import Listing`.<br>Välj [!DNL Commerce] som en matchning till Amazon-attributet för Amazon Seller SKU. Om attributet inte finns, se [Skapa Amazon produktattribut för Amazon Matching](./ob-creating-magento-attributes.md). Granska [!DNL Commerce] [attributes](./managing-attributes.md) och skapa eller redigera ett attribut som matchar dessa Amazon-data. |
| [!UICONTROL Attribute That Contains Amazon ASIN] | Endast aktiv när den är inställd på `Import Listing`.<br>Välj [!DNL Commerce] som matchar Amazon-attributet för Amazon ASIN. Om attributet inte finns, se [Skapa Amazon produktattribut för Amazon Matching](./ob-creating-magento-attributes.md). Granska [!DNL Commerce] [attributes](./managing-attributes.md) och skapa eller redigera ett attribut som matchar dessa Amazon-data. |

**Snabb åtkomst** - [!UICONTROL Listing Settings] avsnitt

- [[!UICONTROL Product Listing Actions]](./product-listing-actions.md)
- [[!UICONTROL Third Party Listings]](./third-party-listing-settings.md)
- [[!UICONTROL Listing Price]](./listing-price.md)
- [[!UICONTROL (B2B) Business Price]](./business-pricing.md)
- [[!UICONTROL Stock / Quantity]](./stock-quantity.md)
- [[!UICONTROL Fulfilled By]](./fulfilled-by.md)
- [[!UICONTROL Catalog Search]](./catalog-search.md)
- [[!UICONTROL Product Listing Condition]](./product-listing-condition.md)
