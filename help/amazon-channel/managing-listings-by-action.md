---
title: Hantera produktlistor efter åtgärd
description: När du hanterar dina Amazon-listor kan du använda en åtgärd på en eller flera listor.
exl-id: 1cbf16fb-15eb-484b-bea7-28017a0d0c60
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%

---

# Hantera produktlistor efter åtgärd

The _[!UICONTROL Product Listings]_-sidan innehåller flera flikar från vilka du kan visa status för alla dina listor och matcha dina produkter med Amazon-listor.

Vilka listuppgifter som är tillgängliga skiljer sig något mellan flikarna, men [arbetsytekontroller](./workspace-controls.md) är samma och gör att du kan anpassa de data som visas för dina listor.

Alternativ under **[!UICONTROL Actions]** kan tillämpa åtgärden på flera listor, medan alternativ under **[!UICONTROL Select]** i _[!UICONTROL Action]_används åtgärden endast på den enskilda listan.

Se även [Hantera listor efter status/flik](./managing-listings-by-tab.md).

| Åtgärd | Beskrivning | Tabbar |
|--- |--- |--- |
| [[!UICONTROL Re-attempt auto match to Amazon Listing]](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) | Används för att flytta de ofullständiga produkterna tillbaka genom matchningsprocessen. Om du vill försöka matcha igen måste du ändra [Lista](./listing-settings.md) och [Katalogsökning](./catalog-search.md) för att öka möjligheten till automatisk matchning. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md) | Matcha katalogprodukterna manuellt med Amazon-listor genom att välja en lista som ska matchas, ange ett ASIN-nummer som ska matchas eller tilldela ett saknat villkor. | [[!UICONTROL Incomplete]](./incomplete-listings.md) |
| [[!UICONTROL View Details]](./product-listing-details.md) | Visa ytterligare information om dina aktiva produkter, inklusive aktivitetsloggen för listning, som visar ändringarna för en enskild SKU/produkt. | [[!UICONTROL Incomplete]](./incomplete-listings.md)<br>[[!UICONTROL New Third Party]](./new-third-party-listings.md)<br>[[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Create New Catalog Product(s)]](./creating-assigning-catalog-products.md) | Skapa en [!DNL Commerce] katalogprodukt med hjälp av den information som importeras tillsammans med Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| Försök att matcha automatiskt | Försök att matcha automatiskt [!DNL Commerce] katalogen och dina Amazon-listor baserat på sökkriteriernas inställningar. Om du vill försöka matcha igen måste du ändra [Lista](./listing-settings.md) och [Katalogsökning](./catalog-search.md) för att öka möjligheten till automatisk matchning. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md) | Välj en befintlig produkt i [!DNL Commerce] och tilldela den till Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md) | Skapa en [!DNL Commerce] katalogprodukt med hjälp av den information som importeras tillsammans med Amazon. | [[!UICONTROL New Third Party]](./new-third-party-listings.md) |
| [[!UICONTROL Publish Product to Amazon]](./publish-listings-manually.md) | (Massåtgärd) Används för att omlista en lista som har avslutats eller för att manuellt lista en produkt som uppfyller dina listregler, men som _[!UICONTROL Product Listing Actions]_är inte inställd på `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Publish On Amazon]](./publish-listings-manually.md) | (En liståtgärd) Används för att lista om en lista som har avslutats. Den här åtgärden används även för att manuellt visa en lista över en produkt som uppfyller dina listregler som är berättigad när _[!UICONTROL Product Listing Actions]_är inte inställd på `Automatically list new products`. | [[!UICONTROL Ready to List]](./ready-to-list.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL End Listing(s) on Amazon]](./end-listings-manually.md) | (Massåtgärd) Används för att manuellt avsluta och ta bort listor för produkter som finns i Amazon. Du kan visa slutna listor på nytt så länge som de uppfyller dina listregler. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Listing Overrides]](./creating-editing-overrides.md) | (Massåtgärd) Redigera en befintlig åsidosättning manuellt som ställer in pris, hanteringstid, villkor och säljarens anteckningstext för en enskild lista, och ignorerar andra liststandarder, inställningar och regler. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Overrides]](./overrides.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Override]](./creating-editing-overrides.md) | Skapa manuellt en&quot;åsidosättning&quot; som anger pris, hanteringstid, villkor och säljarens anteckningstext för en enskild lista, och ignorera andra liststandarder, inställningar och regler. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md) | Används om ASIN som matchar din katalogprodukt måste ändras (exempel: om produkten matchades till fel ASIN-lista). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md) | Kan fungera med två funktioner:<br><br>Kan användas för att skapa en 1:2-relation mellan katalogprodukten och två Amazon-listor. Exempel: Amazon har den produkt som listas med olika ASIN-värden. Du kan matcha din katalogprodukt med båda ASIN-listorna för produkten.<br><br>Kan användas för att styra en lista i olika Amazon-regioner. Exempel: Du har en katalogprodukt som har olika leveransmetoder definierade baserat på Amazon (USA är FBA och Kanada är FBM). Om du vill kontrollera lager/kvantitet kan du skapa en aliasförsäljar-SKU och lista om samma produkt i det området med en annan säljar-SKU. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md)<br>[[!UICONTROL Ended]](./ended-listings.md) |
| [[!UICONTROL Switch to Fulfilled by Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings) | Används för att ändra den leveransmetod som är kopplad till din produkt (som fyllts i av Amazon: FBA eller Fulfill by Merchant: FBM). | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL End Listing]](./end-listings-manually.md) | (En liståtgärd) Används för att manuellt avsluta och ta bort listor för produkter som finns i Amazon. Du kan visa slutna listor på nytt så länge som de uppfyller dina listregler. | [[!UICONTROL Inactive]](./inactive-listings.md)<br>[[!UICONTROL Active]](./active-listings.md)<br>[[!UICONTROL Ineligible]](./ineligible-listings.md) |
| [[!UICONTROL Edit Override]](./creating-editing-overrides.md) | (En liståtgärd) Redigera en befintlig åsidosättning manuellt som anger pris, hanteringstid, villkor och säljarens anteckningstext för en enskild lista, och ignorerar andra liststandarder, inställningar och regler. | [[!UICONTROL Overrides]](./overrides.md) |

## Få tillgång till produktlistor

1. På _Administratör_ sidebar, gå till **Marknadsföring** > _Kanaler_ > **Amazon Sales Channel**.

1. Klicka **Visa butik** på butikskortet.

1. Klicka på **Hantera listor** i _Lagra listor_ -avsnitt.
