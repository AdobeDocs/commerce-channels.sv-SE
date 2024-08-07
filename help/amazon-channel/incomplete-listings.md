---
title: Ofullständiga Amazon-listor
description: Amazon försäljningskanal innehåller fliken [!UICONTROL Incomplete] som hjälper dig att identifiera och uppfylla behörighetskraven för dina ofullständiga Amazon-listor.
feature: Sales Channels, Products
exl-id: f943c9cc-fa1d-4f3e-a3de-3a8d00f87890
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# Ofullständiga Amazon-listor

På fliken _[!UICONTROL Incomplete]_visas de [!DNL Commerce] katalogprodukter som uppfyller dina Amazon behörighetskrav (som definieras i [listreglerna](./listing-rules.md)), men som saknar information som krävs av Amazon (till exempel Amazon ASIN eller ett definierat produktvillkor).

Det finns fyra möjliga orsaker till en ofullständig lista, som alla identifieras av dess status.

| Status | Orsak | Åtgärd |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Villkor saknas | Amazon accepterar listor under olika förhållanden (till exempel _Nytt_, _Återanvänt_, _Använt: Som nytt_) kräver ett definierat villkor. | Uppdatera nödvändig information och [tilldela ett villkor](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) manuellt till en lista. |
| Det går inte att tilldela till Amazon-listan | Det gick inte att matcha den här listan automatiskt med katalogen. Om ingen matchning hittas kan listan inte hanteras av Amazon Sales Channel | Uppdatera nödvändig information och [tilldela katalogprodukten ett ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) manuellt för matchning till listan. |
| Flera träffar hittades | Det gick inte att matcha den här listan automatiskt med katalogen. Om det finns flera möjliga matchningar måste du välja rätt matchning för produkten. | Uppdatera nödvändig information och [välj manuellt en produktmatchning](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) för produkten och listan. |
| Har varianter | Om din produkt har varianter, t.ex. en t-shirt som är tillgänglig i olika storlekar eller färger, måste du välja varianten i din katalog för att kunna tilldelas och matchas korrekt med listan | Uppdatera nödvändig information och [välj manuellt rätt variant](./amazon-manually-update-incomplete-listing.md#update-required-info-has-variants) för att tilldela och matcha den här listan. |

>[!NOTE]
>När ofullständiga listor matchas korrekt med dina katalogprodukter flyttas listan från fliken _[!UICONTROL Incomplete]_och publiceras till Amazon baserat på dina [_[!UICONTROL Product Listing Actions]_](./product-listing-actions.md)-inställningar.

De tillgängliga åtgärderna på fliken _[!UICONTROL Incomplete]_omfattar:

Under _[!UICONTROL Actions]_:

- **[!UICONTROL Re-attempt to auto match to Amazon listings]**: Välj att starta den automatiska processen för att matcha dina Amazon listningsdata med din [!DNL Commerce] -katalog. Om produkterna inte matchar automatiskt kan du gå igenom dina [_[!UICONTROL Catalog Search]_](./catalog-search.md)-alternativ i dina listmeddelanden. Om listor inte matchar automatiskt efter att du har uppdaterat dina _[!UICONTROL Catalog Search]_-alternativ kan du matcha produkter manuellt i [[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found)-åtgärden.

Under **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_:

- **[!UICONTROL Update Required Info]**: Välj när listor inte automatiskt matchar katalogen. Du kan [matcha katalogprodukter mot listor](./amazon-manually-update-incomplete-listing.md#update-required-info-multiple-matches-found) manuellt, [tilldela ett ASIN](./amazon-manually-update-incomplete-listing.md#update-required-info-unable-to-assign-to-amazon-listing) till en katalogmatchning manuellt eller [tilldela ett saknat villkor](./amazon-manually-update-incomplete-listing.md#update-required-info-missing-condition) för listning.

- **[!UICONTROL View Details]**: Välj om du vill visa listinformation, inklusive [Listing Activity Log](./product-listing-details.md#listing-activity-log), [Buy Box Competitor Pricing](./product-listing-details.md#buy-box-competitor-pricing) och [Lowest Competitor Pricing](./product-listing-details.md#lowest-competitor-pricing). Den här åtgärden är endast avsedd för visning. Inga ändringar kan göras i listinformationen. Se [Visa detaljer](./product-listing-details.md).

>[!NOTE]
>
>Om du har pågående listor visas antalet listor i ett meddelande ovanför flikarna.

![Ofullständiga Amazon-listor](assets/amazon-incomplete-listings.png){width="600" zoomable="yes"}

Amazon hemsidor för försäljningskanaler delar några vanliga [arbetsytekontroller](./workspace-controls.md) som gör att du kan anpassa de data som visas.

| Kolumn | Beskrivning |
|-----------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [!UICONTROL Amazon Seller SKU] | SKU (Stock Keeping Unit) som Amazon har tilldelat en produkt för att identifiera produkt, alternativ, pris och tillverkare. |
| [!UICONTROL ASIN] | Ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt.<br><br>ASIN står för [!DNL Amazon Standard Identification Number]. Ett ASIN är ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt. För böcker är ASIN samma som ISBN-numret, men för alla andra produkter skapas ett nytt ASIN när artikeln överförs till sin katalog. Du hittar ett ASIN-objekt på produktinformationssidan på Amazon, tillsammans med mer information om artikeln. |
| [!UICONTROL Product Listing Name] | Produktens namn. |
| [!UICONTROL Condition] | Produktens [villkor](./product-listing-condition.md). |
| [!UICONTROL Landed Price] | Produktens listpris plus dess fraktpris. |
| [!UICONTROL Amazon Quantity] | Kvantiteten som är tillgänglig när produkten är aktivt listad på Amazon. |
| [!UICONTROL Status] | Status för listan, definierad av Amazon. Se tabellen Status ovan. |
| [!UICONTROL Action] | Lista över tillgängliga åtgärder som kan tillämpas på en viss lista. Om du vill använda en åtgärd klickar du på **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_och väljer ett alternativ:<ul><li>[[!UICONTROL Update Required Info]](./amazon-manually-update-incomplete-listing.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
