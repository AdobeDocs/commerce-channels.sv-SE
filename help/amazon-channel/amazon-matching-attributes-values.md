---
title: Visa Amazon-attributmappning
description: Verifiera värden för dina länkade Commerce-attribut så att de synkroniseras korrekt mellan Commerce och Amazon.
feature: Sales Channels, Products, Configuration
exl-id: 11a1fb25-6aa8-43d3-b5d8-772bbe1a5d53
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# Visa Amazon-attributmappning

När du mappar Amazon-attribut till [!DNL Commerce] attribut, Amazon säljkanalsspår och en filterbar lista med alla Amazon-värden. Använd den här sidan om du vill verifiera värden för den länkade [!DNL Commerce] attribut synkroniseras korrekt mellan [!DNL Commerce] och Amazon. Du kan granska synkroniserade värden för Amazon-attribut som är länkade eller inte länkade till en [!DNL Commerce] -attribut. Information om hur du skapar eller redigerar Amazon-attribut finns i [Skapa och redigera attribut](./creating-attributes.md).

The _Amazon Value_ varierar beroende på vilken attributtyp och vilket Amazon-attribut du ser. Till exempel ett Amazon-värde i listan `Label` skulle vara ett textvärde medan `AmazonListPrice` skulle vara ett numeriskt belopp. Statusen anger om Amazon-värdet har importerats.

## Visa dina attributvärden

1. På _[!UICONTROL Admin]_sidebar, gå till **[!UICONTROL Marketing]**>_[!UICONTROL Channels]_ > **[!UICONTROL Amazon Sales Channel]**.

1. Klicka **[!UICONTROL Attributes]** i den vänstra menyn letar du reda på ett Amazon-attribut och klickar på **[!UICONTROL Create]** eller **[!UICONTROL Edit]** i _[!UICONTROL Action]_kolumn.

1. Klicka på **[!UICONTROL Matching Attribute Values]** -fliken.

   Listor som har en motsvarande [!DNL Commerce] katalogprodukten visar ett länkat värde i _[!UICONTROL Magento Product SKU]_kolumn. Om du klickar på en länk öppnas motsvarande katalogproduktinformationssida. Ändringar av Amazon-attribut på produktinformationssidan synkroniseras inte tillbaka till Amazon försäljningskanal.

>[!TIP]
>Information om hur du redigerar eller tilldelar mappning för en lista till en katalogprodukt finns i [Uppdatera obligatorisk information](./amazon-manually-update-incomplete-listing.md).

![Visa attributvärden](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Region] | Regionen för försäljningsaktivitet som definieras i **[!DNL Amazon Marketplace]Land** under butiksintegrering. |
| [!UICONTROL Magento Product SKU] | Anger [!DNL Commerce] produkter som synkroniseras med Amazon Store. Värdet är ett produkt-ID som tilldelats av [!DNL Commerce] och länkas till en produkt i katalogen. Öppna produkten i [!DNL Commerce]klickar du på länken. |
| [!UICONTROL ASIN] | Anger den 10-ställiga alfanumeriska unika identifierare som Amazon har tilldelat produkten för att identifiera produkten. |
| [!UICONTROL Amazon Value] | Anger värdet för det valda attributet. Amazon-värdet skiljer sig åt beroende på vilken attributtyp och vilket Amazon-attribut du ser. Till exempel ett Amazon-värde i listan `Label` skulle vara ett textvärde medan `AmazonListPrice` skulle vara ett numeriskt belopp. Statusen anger om Amazon-värdet har importerats. |
| [!UICONTROL Status] | Anger om attributvärdena har importerats till [!DNL Commerce] och länkas till en [!DNL Commerce] -attribut. Alternativ: `Not Imported` / `Imported` |
