---
title: Uppdatera nödvändig information för Amazon
description: Amazon försäljningskanal innehåller fliken Ofullständig för att övervaka Commerce katalogprodukter som saknar information som Amazon kräver.
feature: Sales Channels, Merchandising, Catalog Management, Products
exl-id: f278cd50-8f04-452e-b9c2-c87820f9faf2
source-git-commit: 8c72b7db5472a573bd8c26acafdf7a3400875477
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---

# Uppdatera obligatorisk information (ofullständig lista)

Listor som visas på fliken _[!UICONTROL Incomplete]_innehåller dina [!DNL Commerce]-katalogprodukter som uppfyller dina Amazon behörighetskrav enligt dina listregler, men som saknar information som Amazon kräver före listningen.

## Uppdatera nödvändig information (det går inte att tilldela till Amazon lista) {#update-required-info-unable-to-assign-to-amazon-listing}

1. Visa listorna på fliken _[!UICONTROL Incomplete]_i [Hantera listor](./managing-product-listings.md).

1. I kolumnen _[!UICONTROL Action]_klickar du på&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**för den lista du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. För **[!UICONTROL Assign ASIN]** anger du det ASIN som tilldelats av Amazon för den lista som du vill matcha med katalogprodukten.

1. Klicka på **[!UICONTROL Save Listing Update]** om du vill spara produktmatchningen.

Listan matchar nu din katalog, och sedan uppdateras den och publiceras till Amazon utifrån dina inställningar för kron och lista. Den tas också bort från fliken _[!UICONTROL Incomplete]_.

![Tilldela ASIN manuellt för ingen matchning av lista](assets/amazon-listing-update-assign-asin.png){width="600" zoomable="yes"}

## Uppdatera nödvändig information (flera träffar hittades) {#update-required-info-multiple-matches-found}

1. Visa listor på fliken _[!UICONTROL Incomplete]_i [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. I kolumnen _Åtgärd_ klickar du på **Välj** > **Uppdatera obligatorisk information** för den lista du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. För **[!UICONTROL Select Correct Amazon Listing]** väljer du rätt ASIN för den lista som du vill matcha med den här produkten.

   De alternativ som anges här omfattar katalogprodukter som identifieras som möjliga matchningar. Om inget av alternativen är korrekt kan du välja `Manually Enter Correct ASIN` och manuellt ange ASIN för produkten.

1. Om du anger ASIN manuellt anger du korrekt ASIN för **[!UICONTROL Manually Assign ASIN]**.

1. Klicka på **[!UICONTROL Save Listing Update]** om du vill spara produktmatchningen.

![Välj ASIN manuellt från flera möjliga matchningar](assets/amazon-listing-update-multiple-matches.png){width="600" zoomable="yes"}

## Uppdatera obligatorisk information (har varianter) {#update-required-info-has-variants}

1. Visa listor på fliken _[!UICONTROL Incomplete]_i [[!UICONTROL Manage Listings]](./managing-product-listings.md).

1. I kolumnen _[!UICONTROL Action]_klickar du på&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**för den lista du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. För **[!UICONTROL Select Correct Amazon Listing]** väljer du rätt ASIN för den lista som du vill matcha med den här produkten.

   De alternativ som anges här omfattar katalogprodukter som identifieras som möjliga matchningar. Om inget av alternativen är korrekt kan du välja `Manually Enter Correct ASIN` och manuellt ange ASIN för produkten.

1. Om du anger ASIN manuellt anger du korrekt ASIN för **[!UICONTROL Manually Assign ASIN]**.

1. Klicka på **[!UICONTROL Save Listing Update]** om du vill spara produktmatchningen.

## Uppdatera nödvändig information (villkor saknas) {#update-required-info-missing-condition}

1. Visa listorna på fliken _[!UICONTROL Incomplete]_i [Hantera listor](./managing-product-listings.md).

1. I kolumnen _[!UICONTROL Action]_klickar du på&#x200B;**[!UICONTROL Select]**>**[!UICONTROL Update Required Info]**för den lista du vill uppdatera.

1. Granska den katalogproduktinformation (SKU och produktnamn) som du försöker matcha mot en Amazon-lista.

1. Välj lämpligt villkor för **[!UICONTROL Condition]**.

   Listan med tillgängliga alternativ beror på inställningarna för [Villkor för produktlista](./product-listing-condition.md).

1. Klicka på **[!UICONTROL Save Listing Update]** om du vill spara produktmatchningen.

![Uppdatera saknat villkor manuellt](assets/amazon-update-listing-missing-condition.png){width="600" zoomable="yes"}
