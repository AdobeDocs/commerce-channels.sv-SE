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

Sidan _[!UICONTROL Product Listings]_innehåller flera flikar från vilka du kan visa status för alla dina listor och matcha dina produkter med Amazon-listor.

Vilka listuppgifter som är tillgängliga skiljer sig något på varje flik, men [arbetsytekontrollerna](./workspace-controls.md) är desamma och gör att du kan anpassa de data som visas för dina listor.

Alternativ under **[!UICONTROL Actions]** kan tillämpa åtgärden på flera listor, medan alternativ under **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_endast tillämpar åtgärden på den enskilda listan.

Se även [Hantera listor efter åtgärd](./managing-listings-by-action.md).

![Flikar för produktlistor](assets/amazon-product-listings-tabs.png){width="600" zoomable="yes"}

| Tabb | Beskrivning | Åtgärder |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Incomplete]](./incomplete-listings.md) | Visar dina [!DNL Commerce]-katalogprodukter som uppfyller dina definierade listinställningar, men som saknar information som krävs av Amazon för en lista.<br><br>Om _[!UICONTROL Automatic List Action]_är inställt på `Automatically List Eligible Products` i dina [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md)-inställningar är dessa objekt din **[!UICONTROL In Progress Listings]**. | [!UICONTROL Reattempt auto match to Amazon Listing]<br>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL New Third Party]](./new-third-party-listings.md) | Visar dina befintliga Amazon-listor (baserat på information som du fått från Amazon) som inte matchar någon produkt i din [!DNL Commerce]-katalog. | [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md)<br>Försök att matcha automatiskt<br>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ready to List]](./ready-to-list.md) | Visar katalogprodukter som är klara att skapa Amazon-listor, men butiken är inställd på att inte automatiskt publicera nya listor. Den här fliken används för att publicera dina nya listor manuellt.<br><br>Om _[!UICONTROL Automatic List Action]_är inställt på `Do Not Automatically List Eligible Products` i dina [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md)-inställningar är dessa objekt din **[!UICONTROL In Progress Listings]**. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Inactive]](./inactive-listings.md) | Visar dina katalogprodukter som har publicerats till Amazon, men Amazon har inte godkänt listan med aktiv status. | [Slut Lista(er) på Amazon](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Växla till Uppfyllt av Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Active]](./active-listings.md) | Visar dina Amazon-listor som har matchats med en produkt i din [!DNL Commerce]-katalog, som har publicerats till Amazon och som har publicerats av Amazon för aktiv status. | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Växla till fyllt av Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Overrides]](./overrides.md) | Visar de Amazon-listor som uppfyller villkoren för en definierad åsidosättning och som åsidosättningen har tillämpats på. Åsidosättningar prioriteras framför andra kontoinställningar. | [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md) |
| [[!UICONTROL Ineligible]](./ineligible-listings.md) | Visar befintliga Amazon-listor som inte längre är berättigade, baserat på dina definierade [listinställningar](./listing-settings.md). | [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md)<br>[[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Create Override]](./creating-editing-overrides.md)<br>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)<br>Växla till fyllt av Amazon/Merchant<br>[[!UICONTROL End Listing]](./end-listings-manually.md) |
| [[!UICONTROL Ended]](./ended-listings.md) | Visar de Amazon-listor som manuellt har avslutats (tagits bort) från Amazon. | [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL View Details]](./product-listing-details.md)<br>[[!UICONTROL Publish On Amazon]](./publish-listings-manually.md)<br>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific) |

## Få tillgång till produktlistor

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**på sidofältet_ Admin _.

1. Klicka på **[!UICONTROL View Store]** på butikskortet.

1. Klicka på **[!UICONTROL Manage Listings]** i avsnittet _[!UICONTROL Store Listings]_på butikspanelen.
