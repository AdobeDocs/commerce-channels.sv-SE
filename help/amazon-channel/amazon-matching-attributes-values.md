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

När du mappar Amazon-attribut till [!DNL Commerce]-attribut spåras Amazon försäljningskanal och en filterbar lista med alla Amazon-värden visas. Använd den här sidan om du vill verifiera värden för dina länkade [!DNL Commerce]-attribut som synkroniseras korrekt mellan [!DNL Commerce] och Amazon. Du kan granska synkroniserade värden för Amazon-attribut som är länkade eller inte länkade till ett [!DNL Commerce]-attribut. Mer information om hur du skapar eller redigerar Amazon-attribut finns i [Skapa och redigera attribut](./creating-attributes.md).

_Amazon-värdet_ skiljer sig åt beroende på vilken attributtyp och vilket Amazon-attribut du visar. Ett angivet Amazon-värde för `Label` skulle till exempel vara ett textvärde medan `AmazonListPrice` skulle vara ett numeriskt värde. Statusen anger om Amazon-värdet har importerats.

## Visa dina attributvärden

1. Gå till **[!UICONTROL Marketing]** > _[!UICONTROL Channels]_>**[!UICONTROL Amazon Sales Channel]**på sidofältet_[!UICONTROL Admin]_.

1. Klicka på **[!UICONTROL Attributes]** på den vänstra menyn, leta upp ett Amazon-attribut och klicka på antingen **[!UICONTROL Create]** eller **[!UICONTROL Edit]** i kolumnen _[!UICONTROL Action]_.

1. Klicka på fliken **[!UICONTROL Matching Attribute Values]**.

   Listor som har en motsvarande [!DNL Commerce]-katalogprodukt visar ett länkat värde i kolumnen _[!UICONTROL Magento Product SKU]_. Om du klickar på en länk öppnas motsvarande katalogproduktinformationssida. Ändringar av Amazon-attribut på produktinformationssidan synkroniseras inte tillbaka till Amazon försäljningskanal.

>[!TIP]
>Mer information om hur du redigerar eller tilldelar mappningen för en lista till en katalogprodukt finns i [Uppdatera obligatorisk information](./amazon-manually-update-incomplete-listing.md).

![Visa attributvärden](assets/amazon-managing-attribute-values.png){width="600" zoomable="yes"}

| Fält | Beskrivning |
|----------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Region] | Regionen för försäljningsaktivitet som definieras i **[!DNL Amazon Marketplace]Country** under butiksintegrering. |
| [!UICONTROL Magento Product SKU] | Anger vilka [!DNL Commerce]-produkter som har synkroniserats med Amazon Store. Värdet är ett produkt-ID som tilldelats av [!DNL Commerce] och som är länkat till en produkt i katalogen. Klicka på länken om du vill öppna produkten i [!DNL Commerce]. |
| [!UICONTROL ASIN] | Anger den 10-ställiga alfanumeriska unika identifierare som Amazon har tilldelat produkten för att identifiera produkten. |
| [!UICONTROL Amazon Value] | Anger värdet för det valda attributet. Amazon-värdet skiljer sig åt beroende på vilken attributtyp och vilket Amazon-attribut du ser. Ett angivet Amazon-värde för `Label` skulle till exempel vara ett textvärde medan `AmazonListPrice` skulle vara ett numeriskt värde. Statusen anger om Amazon-värdet har importerats. |
| [!UICONTROL Status] | Anger om attributvärdena har importerats till [!DNL Commerce] och länkats till ett [!DNL Commerce]-attribut. Alternativ: `Not Imported` / `Imported` |
