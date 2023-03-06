---
title: Nya tredjepartslistor
description: Hantera nya Amazon-listor genom att matcha dem med en produkt i din Commerce-katalog.
exl-id: ace9d334-d1d1-4f4b-88c8-60a9e7d1d17c
source-git-commit: b63e2cfb9c7ba7cc169a6eec954abe782d112c6f
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 0%

---

# Nya tredjepartslistor

The _[!UICONTROL New Third Party]_visas dina befintliga Amazon-listor som inte har matchats mot en produkt i [!DNL Commerce] katalog. Om du vill använda listhantering för kvantitet, priser, hanteringstid med mera måste alla dina Amazon-listor matchas (tilldelas) till en produkt i din [!DNL Commerce] katalog. Du kan tilldela en produkt i din [!DNL Commerce] katalog.

Under _[!UICONTROL Actions]_:

- **[!UICONTROL Create New Catalog Product(s)]**: Välj om du vill använda informationen i Amazon lista för att automatiskt skapa en produkt i [!DNL Commerce] katalog. Den här processen matchar Amazon lista automatiskt med den nya katalogprodukten. Se [Skapa och tilldela katalogprodukter](./creating-assigning-catalog-products.md).

- **[!UICONTROL Attempt Automatic Match]**: Välj om du vill försöka matcha automatiskt de markerade listorna mot din katalog baserat på din aktuella [Katalogsökning](./catalog-search.md) i listinställningarna. Om du ändrar dina _[!UICONTROL Catalog Search]_kan du med den här åtgärden försöka matcha processen igen.

Under _[!UICONTROL Select]_:

- **[!UICONTROL Assign Catalog Product]**: Välj om du vill matcha listan med en produkt i din [!DNL Commerce] katalog manuellt. Se [Skapa och tilldela katalogprodukter](./creating-assigning-catalog-products.md).

- **[!UICONTROL Create New Catalog Product]**: Välj om du vill använda informationen i Amazon lista för att automatiskt skapa en produkt i [!DNL Commerce] katalog. Den här processen matchar Amazon lista automatiskt med den nya katalogprodukten. Se [Skapa och tilldela katalogprodukter](./creating-assigning-catalog-products.md).

- **[!UICONTROL View Details]**: Välj om du vill visa listinformation, inklusive [Logg för listaktivitet](./product-listing-details.md#listing-activity-log), [Buy Boxens konkurrentpriser](./product-listing-details.md#buy-box-competitor-pricing)och [Lägsta konkurrentpris](./product-listing-details.md#lowest-competitor-pricing). Den här åtgärden är endast avsedd för visning. Inga ändringar kan göras i listinformationen. Se [Visa detaljer](./product-listing-details.md).

>[!NOTE]
>
>Om du har pågående listor visas ett meddelande ovanför flikarna som anger antalet listor.

![Nya listor från tredje part](assets/amazon-listings-new-third-party.png)

Amazon hemsidor för försäljningskanaler delar några vanliga sidor [arbetsytekontroller](./workspace-controls.md) som gör att du kan anpassa de data som visas.

## Standardkolumner

| Kolumn | Beskrivning |
|---|---|
| [!UICONTROL Amazon Seller SKU] | SKU (Stock Keeping Unit) som Amazon har tilldelat en produkt för att identifiera produkt, alternativ, pris och tillverkare. |
| [!UICONTROL ASIN] | Ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt.<br><br>ASIN står för [!DNL Amazon Standard Identification Number]. Ett ASIN är ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt. För böcker är ASIN samma som ISBN-numret, men för alla andra produkter skapas ett nytt ASIN när artikeln överförs till sin katalog. Du hittar ett ASIN-objekt på produktinformationssidan på Amazon, tillsammans med mer information om artikeln. |
| [!UICONTROL Product Listing Name] | Produktens namn. |
| [!UICONTROL Condition] | The [villkor](./product-listing-condition.md) av produkten. |
| [!UICONTROL Listing Price] | Identifierar artikelns listpris, definierat av priskällan och eventuella tillämpliga prisregler. |
| [!UICONTROL Amazon Quantity] | Kvantiteten som är tillgänglig när produkten är aktivt listad på Amazon. |
| [!UICONTROL Status] | Status för listan, definierad av Amazon. |
| [!UICONTROL Action] | Lista över tillgängliga åtgärder som kan tillämpas på en viss lista. Om du vill använda en åtgärd klickar du på **[!UICONTROL Select]** i _[!UICONTROL Action]_och välj ett alternativ:<ul><li>[[!UICONTROL Assign Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL Create New Catalog Product]](./creating-assigning-catalog-products.md)</li><li>[[!UICONTROL View Details]](./product-listing-details.md)</li></ul> |
