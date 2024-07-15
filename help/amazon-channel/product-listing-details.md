---
title: Visa Amazon listinformation
description: Om du vill veta mer om konkurrensstatistik för dina Amazon-listor och om enskilda SKU-/produktändringar kan du gå till sidan Produktlistningsinformation.
feature: Sales Channels, Products, Merchandising
exl-id: faece1b1-b4fb-4506-bf77-576ae445ed28
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# Visa Amazon listinformation

På sidan _[!UICONTROL Product Listing Details]_visas ytterligare information om dina aktiva produktlistor, inklusive aktivitetsloggen för listning som visar ändringarna för en enskild SKU/produkt. Denna information kan hjälpa er att förstå konkurrensstatistik för era produkter och om individuella SKU-/produktförändringar. Ytterligare information på den här sidan innehåller:

- **[!UICONTROL Listing Details]** - Produktinformation inklusive namn och Amazon Seller SKU
- **[!UICONTROL Listing Activity Log]** - Historik över alla ändringar som har gjorts för den här listan, till exempel prissättning och kvantitet/lagerändringar. Inga fler åtgärder krävs. Den här loggen finns för granskning för att förstå ändringshistoriken.
- **[!UICONTROL Buy Box Competitor Pricing]** - Data för Amazon [[!DNL Buy Box]](./buy-box-competitor-pricing.md)-status och konkurrentpriser
- **[!UICONTROL Lowest Competitor Pricing]** - Information om den lägsta Amazon-konkurrentens priser och feedback-information

Amazon hemsidor för försäljningskanaler delar några vanliga [arbetsytekontroller](./workspace-controls.md) som gör att du kan anpassa de data som visas.

## Listinformation

Den produktinformation som visas omfattar:

- _[!UICONTROL Amazon Name]_
- _[!UICONTROL Catalog (Magento) SKU]_
- _[!UICONTROL Amazon Seller SKU]_

![Listinformation](assets/amazon-product-listing-details.png){width="600" zoomable="yes"}

## Logg för listningsaktivitet {#listing-activity-log}

Visar alla senaste aktiviteter för Amazon-listan. Följande information visas:

- Amazon Seller SKU: Identifierar den SKU (Stock Keeping Unit) som definierats för förteckningen.
- ASIN: Identifierar den 10-siffriga Amazon-produktidentifieraren.
- Liståtgärd: Identifierar typen av åtgärd som inträffade för listan.
- Kommentarer: Ger ytterligare information om vilken typ av liståtgärd som har utförts.
- Körd: Identifierar datum och tid då åtgärden utfördes.

![Produktlistningsinformation - Visar aktivitetslogg](assets/amazon-listing-activity-log.png){width="600" zoomable="yes"}
__

## Buy Boxens konkurrentpriser {#buy-box-competitor-pricing}

På den här fliken visas information om den Amazon-handlare som har positionen [[!DNL Buy Box]](./buy-box-competitor-pricing.md) för listan. Denna information kan användas för att förstå prisplaceringen för dina konkurrenter på Amazon. Följande information visas:

- ASIN: Den 10-siffriga Amazon-produktidentifieraren.
- Är säljare: Identifierar om du är [!DNL Buy Box]-säljaren. Alternativ Ja/Nej
- Villkor: Identifierar det villkor som definierats för listan.
- Listing Price: Identifierar det pris till vilket noteringen publicerades.
- Leveranspris: Identifierar det leveranspris som lagts till i listan.
- Landed Price: Identifierar listpriset plus leveranspriset för noteringen.
- Senast uppdaterad: Anger datum och tid då prisinformationen uppdaterades från Amazon.

![Produktlistningsinformation: Buy Box konkurrentpriser](assets/amazon-listing-details-buy-box-2.png){width="600" zoomable="yes"}

## Lägsta konkurrentpris {#lowest-competitor-pricing}

På den här fliken visas information om Amazon konkurrenter för samma lista. Den här informationen kan användas för att förstå prispositionering och [lägsta konkurrentpris](./lowest-competitor-pricing.md). Följande information visas:

- ASIN: Den 10-siffriga Amazon-produktidentifieraren.
- Villkor: Identifierar det villkor som definierats för listan.
- Fulfillment Channel: Identifierar den part som är ansvarig för uppfyllandet. Alternativ: Merchant/Amazon.
- Listing Price: Identifierar det pris till vilket noteringen publicerades.
- Leveranspris: Identifierar det leveranspris som lagts till i listan.
- Landed Price: Identifierar listpriset plus leveranspriset för noteringen.
- Feedback Rating: Identifierar Amazon feedback Rating for the lower price handlant.
- Feedback Count: Identifierar Amazon feedback count för den lägsta handlaren.
- Senast uppdaterad: Anger datum och tid då prisinformationen uppdaterades från Amazon.

![Produktlistinformation - lägsta konkurrentpris](assets/amazon-listing-details-lowest-comp.png){width="600" zoomable="yes"}
