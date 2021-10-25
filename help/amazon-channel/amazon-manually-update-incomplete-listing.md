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

Listor som visas på _[!UICONTROL Incomplete]_-fliken innehåller [!DNL Commerce] katalogprodukter som uppfyller kraven för Amazon som du har angett i din lista, men som inte innehåller den information som Amazon behöver innan du kan börja använda den.

## Uppdatera nödvändig information (Det går inte att tilldela till Amazon lista) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Visa listorna på _[!UICONTROL Incomplete]_tabba in [Hantera listor](./managing-product-listings.md).

1. I _[!UICONTROL Action]_kolumn, klicka **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**för den lista som du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. För **[!UICONTROL Assign ASIN]** anger du det ASIN som tilldelats av Amazon för den lista som du vill matcha med katalogprodukten.

1. Om du vill spara produktmatchningen klickar du på **[!UICONTROL Save Listing Update]**.

Listan matchar nu din katalog, och sedan uppdateras den och publiceras till Amazon utifrån dina inställningar för kron och lista. Den tas också bort från _[!UICONTROL Incomplete]_-fliken.

![Tilldela ASIN manuellt utan matchning](assets/amazon-listing-update-assign-asin.png)

## Uppdatera nödvändig information (Flera träffar hittades) {#update-required-info-multiple-matches-found}

1. Visa listorna på _[!UICONTROL Incomplete]_tabba in [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. I _Åtgärd_ kolumn, klicka **Välj** > **Uppdatera obligatorisk information** för den lista som du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. För **[!UICONTROL Select Correct Amazon Listing]** väljer du rätt ASIN för den lista som du vill matcha med den här produkten.

   De alternativ som anges här omfattar katalogprodukter som identifieras som möjliga matchningar. Om inget av alternativen är korrekt kan du välja `Manually Enter Correct ASIN` och ange produktens ASIN manuellt.

1. Om du anger ASIN manuellt anger du rätt ASIN för **[!UICONTROL Manually Assign ASIN]**.

1. Om du vill spara produktmatchningen klickar du på **[!UICONTROL Save Listing Update]**.

![Välj ASIN manuellt från flera möjliga matchningar](assets/amazon-listing-update-multiple-matches.png)

## Uppdatera obligatorisk information (har varianter) {#update-required-info-has-variants}

1. Visa listorna på _[!UICONTROL Incomplete]_tabba in [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. I _[!UICONTROL Action]_kolumn, klicka **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**för den lista som du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. För **[!UICONTROL Select Correct Amazon Listing]** väljer du rätt ASIN för den lista som du vill matcha med den här produkten.

   De alternativ som anges här omfattar katalogprodukter som identifieras som möjliga matchningar. Om inget av alternativen är korrekt kan du välja `Manually Enter Correct ASIN` och ange produktens ASIN manuellt.

1. Om du anger ASIN manuellt anger du rätt ASIN för **[!UICONTROL Manually Assign ASIN]**.

1. Om du vill spara produktmatchningen klickar du på **[!UICONTROL Save Listing Update]**.

![Välj ASIN manuellt från möjliga variantmatchningar](assets/amazon-listing-update-multiple-matches.png)

## Uppdatera nödvändig information (villkor saknas) {#update-required-info-missing-condition}

1. Visa listorna på _[!UICONTROL Incomplete]_tabba in [Hantera listor](./managing-product-listings.md).

1. I _[!UICONTROL Action]_kolumn, klicka **[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**för den lista som du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. För **[!UICONTROL Condition]** väljer du lämpligt villkor.

   Listan med tillgängliga alternativ beror på [Villkor för produktlista](./product-listing-condition.md) inställningar.

1. Om du vill spara produktmatchningen klickar du på **[!UICONTROL Save Listing Update]** .

![Uppdatera saknat villkor manuellt](assets/amazon-update-listing-missing-condition.png)
