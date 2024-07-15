---
title: Hantera Amazon produktlistor efter åtgärd
description: När du hanterar dina Amazon-listor kan du använda en åtgärd på en eller flera listor.
feature: Sales Channels, Products
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# Hantera Amazon produktlistor efter åtgärd

Sidan _[!UICONTROL Product Listings]_innehåller flera flikar från vilka du kan visa status för alla dina listor och matcha dina produkter med Amazon-listor.

Vilka listuppgifter som är tillgängliga skiljer sig något på varje flik, men [arbetsytekontrollerna](./workspace-controls.md) är desamma och gör att du kan anpassa de data som visas för dina listor.

Alternativ under **[!UICONTROL Actions]** kan tillämpa åtgärden på flera listor, medan alternativ under **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_endast tillämpar åtgärden på den enskilda listan.

Se även [Hantera listor efter status/flik](./managing-listings-by-tab.md).

| Åtgärd | Beskrivning | Tabbar |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | Används för att flytta de ofullständiga produkterna tillbaka genom matchningsprocessen. Om du vill försöka matcha igen måste du ändra inställningarna för [Listing](./listing-settings.md) och [Catalog Search](./catalog-search.md) för att öka möjligheten till automatisk matchning. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | Matcha katalogprodukterna manuellt med Amazon-listor genom att välja en lista som ska matchas, ange ett ASIN-nummer som ska matchas eller tilldela ett saknat villkor. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | Visa ytterligare information om dina aktiva produkter, inklusive aktivitetsloggen för listning, som visar ändringarna för en enskild SKU/produkt. | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | Skapa en [!DNL Commerce]-katalogprodukt med hjälp av den information som har importerats med Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| Försök att matcha automatiskt | Försök att automatiskt matcha din [!DNL Commerce]-katalog med dina Amazon-listor baserat på sökkriterieinställningarna. Om du vill försöka matcha igen måste du ändra inställningarna för [Listing](./listing-settings.md) och [Catalog Search](./catalog-search.md) för att öka möjligheten till automatisk matchning. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | Välj en befintlig produkt i din [!DNL Commerce]-katalog manuellt och tilldela den till Amazon-listan. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | Skapa en [!DNL Commerce]-katalogprodukt med hjälp av den information som har importerats med Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | (Massåtgärd) Används för att omlista en lista som har avslutats eller för att manuellt lista en produkt som uppfyller dina listregler, men din _[!UICONTROL Product Listing Actions]_är inte inställd på `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | (En liståtgärd) Används för att lista om en lista som har avslutats. Den här åtgärden används även för att manuellt visa en produkt som uppfyller dina listregler som är berättigade när _[!UICONTROL Product Listing Actions]_inte är inställd på `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | (Massåtgärd) Används för att manuellt avsluta och ta bort listor för produkter som finns i Amazon. Du kan visa slutna listor på nytt så länge som de uppfyller dina listregler. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | (Massåtgärd) Redigera en befintlig åsidosättning manuellt som ställer in pris, hanteringstid, villkor och säljarens anteckningstext för en enskild lista, och ignorerar andra liststandarder, inställningar och regler. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | Skapa manuellt en&quot;åsidosättning&quot; som anger pris, hanteringstid, villkor och säljarens anteckningstext för en enskild lista, och ignorera andra liststandarder, inställningar och regler. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | Används om ASIN matchat med din katalogprodukt måste ändras (exempel: om produkten matchades till fel ASIN-lista). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | Kan fungera med två funktioner:<br><br>Kan användas för att skapa en 1:2-relation mellan katalogprodukten och två Amazon-listor. Exempel: Amazon har produkten med olika ASIN-värden. Du kan matcha din katalogprodukt med båda ASIN-listorna för produkten.<br><br>Kan användas för att styra en lista i olika Amazon-regioner. Exempel: Du har en katalogprodukt som har olika leveransmetoder definierade baserat på Amazon (USA är FBA och Kanada är FBM). Om du vill kontrollera lager/kvantitet kan du skapa en aliasförsäljar-SKU och lista om samma produkt i det området med en annan säljar-SKU. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | Används för att ändra den leveransmetod som är kopplad till din produkt (Fylls i av Amazon: FBA eller Fulfill by Merchant: FBM). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | (En liståtgärd) Används för att manuellt avsluta och ta bort listor för produkter som finns i Amazon. Du kan visa slutna listor på nytt så länge som de uppfyller dina listregler. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | (En liståtgärd) Redigera en befintlig åsidosättning manuellt som anger pris, hanteringstid, villkor och säljarens anteckningstext för en enskild lista, och ignorerar andra liststandarder, inställningar och regler. | [[!UICONTROL Overrides]](./overrides.md) |

## Få tillgång till produktlistor

1. Gå till **Markering** > _Kanaler_ > **Amazon-Sales Channel** på sidofältet _Admin_.

1. Klicka på **Visa butik** på butikskortet.

1. Klicka på **Hantera listor** i avsnittet _Butikslistor_ på butikspanelen.
