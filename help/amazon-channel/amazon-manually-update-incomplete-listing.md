---
title: Uppdatera obligatorisk information (ofullständig lista)
description: Amazon försäljningskanal innehåller fliken Ofullständig för att övervaka Commerce Catalog-produkter som saknar information som krävs av Amazon.
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '473'
ht-degree: 0%

---

# Uppdatera obligatorisk information (ofullständig lista)

Listor som visas på fliken _[!UICONTROL Incomplete]_innehåller dina [!DNL Commerce] katalogprodukter som uppfyller dina Amazon behörighetskrav enligt dina listregler, men som saknar information som Amazon behöver innan de listas.

## Uppdatera nödvändig information (Det går inte att tilldela till Amazon lista) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Visa listorna på fliken _[!UICONTROL Incomplete]_i [Hantera listor](./managing-product-listings.md).

1. Klicka på **[!UICONTROL Select]** > **[!UICONTROL Update Required Info]** i kolumnen _[!UICONTROL Action]_för den lista som du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. I **[!UICONTROL Assign ASIN]** anger du det ASIN som tilldelats av Amazon för den lista som du vill matcha med katalogprodukten.

1. Om du vill spara produktmatchningen klickar du på **[!UICONTROL Save Listing Update]**.

Listan matchar nu din katalog, och sedan uppdateras den och publiceras till Amazon utifrån dina inställningar för kron och lista. Den tas också bort från fliken _[!UICONTROL Incomplete]_.

![Tilldela ASIN manuellt utan matchning](assets/amazon-listing-update-assign-asin.png)

## Uppdatera nödvändig information (Flera träffar hittades) {#update-required-info-multiple-matches-found}

1. Visa listorna på fliken _[!UICONTROL Incomplete]_i [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. I kolumnen _Åtgärd_ klickar du på **Välj** > **Uppdatera obligatorisk information** för den lista du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. För **[!UICONTROL Select Correct Amazon Listing]** väljer du rätt ASIN för den lista som du vill matcha med den här produkten.

   De alternativ som anges här omfattar katalogprodukter som identifieras som möjliga matchningar. Om inget av alternativen är korrekt kan du välja `Manually Enter Correct ASIN` och manuellt ange ASIN för produkten.

1. Om du anger ASIN manuellt anger du korrekt ASIN för **[!UICONTROL Manually Assign ASIN]**.

1. Om du vill spara produktmatchningen klickar du på **[!UICONTROL Save Listing Update]**.

![Välj ASIN manuellt från flera möjliga matchningar](assets/amazon-listing-update-multiple-matches.png)

## Uppdatera obligatorisk information (har varianter) {#update-required-info-has-variants}

1. Visa listorna på fliken _[!UICONTROL Incomplete]_i [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. Klicka på **[!UICONTROL Select]** > **[!UICONTROL Update Required Info]** i kolumnen _[!UICONTROL Action]_för den lista som du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. För **[!UICONTROL Select Correct Amazon Listing]** väljer du rätt ASIN för den lista som du vill matcha med den här produkten.

   De alternativ som anges här omfattar katalogprodukter som identifieras som möjliga matchningar. Om inget av alternativen är korrekt kan du välja `Manually Enter Correct ASIN` och manuellt ange ASIN för produkten.

1. Om du anger ASIN manuellt anger du korrekt ASIN för **[!UICONTROL Manually Assign ASIN]**.

1. Om du vill spara produktmatchningen klickar du på **[!UICONTROL Save Listing Update]**.

![Välj ASIN manuellt från möjliga variantmatchningar](assets/amazon-listing-update-multiple-matches.png)

## Uppdatera nödvändig information (villkor saknas) {#update-required-info-missing-condition}

1. Visa listorna på fliken _[!UICONTROL Incomplete]_i [Hantera listor](./managing-product-listings.md).

1. Klicka på **[!UICONTROL Select]** > **[!UICONTROL Update Required Info]** i kolumnen _[!UICONTROL Action]_för den lista som du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. Välj lämpligt villkor för **[!UICONTROL Condition]**.

   Listan med tillgängliga alternativ beror på dina [produktlistvillkor](./product-listing-condition.md)-inställningar.

1. Om du vill spara produktmatchningen klickar du på **[!UICONTROL Save Listing Update]** .

![Uppdatera saknat villkor manuellt](assets/amazon-update-listing-missing-condition.png)
