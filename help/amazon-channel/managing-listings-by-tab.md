---
title: Hantera Amazon produktlistor efter status/flik
description: När du hanterar dina Amazon-listor kan du tillämpa åtgärder på dina listor enligt status.
feature: Sales Channels, Products
exl-id: 33effdd8-baa9-4fc5-8c7e-313175eb7e9c
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Hantera Amazon produktlistor efter status/flik

The _[!UICONTROL Product Listings]_-sidan innehåller flera flikar från vilka du kan visa status för alla dina listor och matcha dina produkter med Amazon-listor.

Vilka listuppgifter som är tillgängliga skiljer sig något mellan flikarna, men [arbetsytekontroller](./workspace-controls.md) är samma och gör att du kan anpassa de data som visas för dina listor.

Alternativ under **[!UICONTROL Actions]** kan tillämpa åtgärden på flera listor, medan alternativ under **[!UICONTROL Select]** i _[!UICONTROL Action]_används åtgärden endast på den enskilda listan.

Se även [Hantera listor efter åtgärd](./managing-listings-by-action.md).

![Flikar för produktlistor](assets/amazon-product-listings-tabs.png){width="600" zoomable="yes"}

| Tabb | Beskrivning | Åtgärder |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Visar dina [!DNL Commerce] katalogprodukter som uppfyller dina definierade listinställningar men som saknar information som krävs av Amazon för en lista.<br><br>If _[!UICONTROL Automatic List Action]_är inställd på `Automatically List Eligible Products` i [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) inställningar, dessa objekt är **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Visar dina befintliga Amazon-listor (baserat på information som du fått från Amazon) som inte matchar någon produkt i din [!DNL Commerce] katalog. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Försök att matcha automatiskt<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Visar katalogprodukter som är klara att skapa Amazon-listor, men butiken är inställd på att inte automatiskt publicera nya listor. Den här fliken används för att publicera dina nya listor manuellt.<br><br>If _[!UICONTROL Automatic List Action]_är inställd på `Do Not Automatically List Eligible Products` i [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md) inställningar, dessa objekt är **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Visar dina katalogprodukter som har publicerats till Amazon, men Amazon har inte godkänt listan med aktiv status. | [End Lista(ar) på Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Byt till Fulfill by Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Visar de Amazon-listor som har matchats mot en produkt i [!DNL Commerce] har publicerats till Amazon och har av Amazon fått statusen Aktiv. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Byt till Fulfill by Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Visar de Amazon-listor som uppfyller villkoren för en definierad åsidosättning och som åsidosättningen har tillämpats på. Åsidosättningar prioriteras framför andra kontoinställningar. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Visar befintliga Amazon-listor som inte längre är berättigade, baserat på dina definierade [listinställningar](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Byt till Fulfill by Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Visar de Amazon-listor som manuellt har avslutats (tagits bort) från Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Få tillgång till produktlistor

1. På _Administratör_ sidebar, gå till **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**.

1. Klicka **[!UICONTROL View Store]** på butikskortet.

1. Klicka på **[!UICONTROL Manage Listings]** i _[!UICONTROL Store Listings]_-avsnitt.
