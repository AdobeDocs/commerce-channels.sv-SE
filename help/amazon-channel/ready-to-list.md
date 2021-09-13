---
title: Klar för lista
description: Amazon försäljningskanal innehåller fliken Klar att lista som hjälper dig att granska Commerce-produkter som uppfyller kraven men som inte listas automatiskt.
exl-id: f62017fb-964f-43f0-b76b-8f39f447466a
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '435'
ht-degree: 0%

---

# [!UICONTROL Ready to List]

På fliken _[!UICONTROL Ready to List]_visas dina [!DNL Commerce]-katalogprodukter som uppfyller dina listinställningar och kan publiceras på Amazon som en **ny**-lista. Till skillnad från andra listflikar visas inte alltid den här fliken på [_[!UICONTROL Product Listings]_](./managing-product-listings.md)-sidan.

Fliken _[!UICONTROL Ready to List]_visas bara när [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) i listinställningarna är `Do Not Automatically List Eligible Products`. Den här inställningen anger för Amazon försäljningskanal att alla nya Amazon-listor måste publiceras manuellt.

När [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) är `Automatically List Eligible Products` kommer Amazon försäljningskanal automatiskt att publicera nya listor för de katalogprodukter som ingår. Eftersom nya listor publiceras automatiskt visas inte fliken _[!UICONTROL Ready to List]_.

Under _[!UICONTROL Actions]_:

- **[!UICONTROL Publish Product to Amazon]**: Välj att publicera om listan till  [!DNL Amazon Marketplace]. Se [Publicera en Amazon-lista](./publish-listings-manually.md)

Under **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_:

- **[!UICONTROL Publish On Amazon]**: Välj att publicera om listan till  [!DNL Amazon Marketplace]. Se [Publicera en Amazon-lista](./publish-listings-manually.md).

- **[!UICONTROL View Details]**: Välj om du vill visa listinformation, inklusive  [listningsaktivitetsloggen](./product-listing-details.md#listing-activity-log),  [Buy Boxens konkurrentpriser](./product-listing-details.md#buy-box-competitor-pricing) och  [lägsta konkurrentpriser](./product-listing-details.md#lowest-competitor-pricing). Den här åtgärden är endast avsedd för visning. Inga ändringar kan göras i listinformationen. Se [Visa detaljer](./product-listing-details.md).

Det finns några alternativ för att manuellt [publicera en ny lista till Amazon](./publish-listings-manually.md).

>[!NOTE]
>Om du har pågående listor visas antalet listor i ett meddelande ovanför flikarna.

![Klar att visas](assets/amazon-ready-to-list.png)

## Standardkolumner

| Kolumn | Beskrivning |
|---|---|
| [!UICONTROL Amazon Seller SKU] | SKU (Stock Keeping Unit) som Amazon har tilldelat en produkt för att identifiera produkt, alternativ, pris och tillverkare. |
| [!UICONTROL ASIN] | Ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt.<br><br>ASIN står för  [!DNL Amazon Standard Identification Number]. Ett ASIN är ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt. För böcker är ASIN samma som ISBN-numret, men för alla andra produkter skapas ett nytt ASIN när objektet överförs till deras katalog. Du hittar ett ASIN-objekt på produktinformationssidan på Amazon, tillsammans med mer information om artikeln. |
| [!UICONTROL Product Listing Name] | Produktens namn. |
| [!UICONTROL Condition] | Produktens [villkor](./product-listing-condition.md). |
| [!UICONTROL Landed Price] | Produktens listpris plus dess fraktpris. |
| [!UICONTROL Amazon Quantity] | Kvantiteten som är tillgänglig när produkten är aktivt listad på Amazon. |
| [!UICONTROL Status] | Status för listan, definierad av Amazon. |
| [!UICONTROL Action] | Lista över tillgängliga åtgärder som kan tillämpas på en viss lista. Om du vill använda en åtgärd klickar du på **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_och väljer ett alternativ:<ul><li>[[!UICONTROL Publish on Amazon]](./publish-listings-manually.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |

### Vanliga orsaker till listor som är klara att listas

- **[!UICONTROL Ready to List]** - Produkten matchas mot ett Amazon ASIN och är schemalagd för listning. Om [**[!UICONTROL Automatic List Action]**](./product-listing-actions.md) i listinställningarna är inställt på `Do Not Automatically List Eligible Products` representerar den här statusen de produkter som är klara att visas manuellt.

- **[!UICONTROL List in Progress]** - Produktlistan har skickats till Amazon och väntar på bekräftelse från Amazon.
