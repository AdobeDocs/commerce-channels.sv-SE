---
title: Aktiva listor
description: Amazon försäljningskanal innehåller fliken Aktiv för att övervaka aktiva Amazon-listor och som matchas mot en produkt i din Adobe Commerce-katalog.
exl-id: c9105abc-74d6-442b-8d7a-e5aaea8872e4
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# Aktiva listor

The _[!UICONTROL Active]_visas dina Amazon-listor som är aktiva på fliken [!DNL Amazon Marketplace] och som har matchats mot en produkt i [!DNL Commerce] katalog.

Tillgängliga åtgärder på _[!UICONTROL Active]_-fliken innehåller:

Under _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: Välj att ta bort alla markerade listor från [!DNL Amazon Marketplace]. Se [Avsluta en Amazon-lista](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: Välj om du vill ändra åsidosättningsinställningarna för listan. Se [Åsidosättningar](./overrides.md) eller [Redigera eller ta bort en åsidosättning](./creating-editing-overrides.md#edit-override-single-listing).

Under **[!UICONTROL Select]** i _[!UICONTROL Action]_kolumn:

- **[!UICONTROL View Details]**: Välj om du vill visa listinformation, inklusive [Logg för listaktivitet](./product-listing-details.md#listing-activity-log), [Buy Boxens konkurrentpriser](./product-listing-details.md#buy-box-competitor-pricing)och [Lägsta konkurrentpris](./product-listing-details.md#lowest-competitor-pricing). Den här åtgärden är endast avsedd för visning. Inga ändringar kan göras i listinformationen. Se [Visa detaljer](./product-listing-details.md).

- **[!UICONTROL Create Override]**: Välj om du vill skapa en åsidosättning och använda den i den här listan. Se [Skapa en åsidosättning](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: Välj om du vill ändra det ASIN som tilldelats katalogprodukten. Använd den här åtgärden om en produkt i din katalog matchades med fel ASIN. Se [Redigera en tilldelad ASIN](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: Välj om du vill skapa en Alias-SKU som kan användas för att skapa en Amazon-lista från samma katalogprodukt. Se [Skapa en SKU för Aliasförsäljare](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: Välj om du vill ändra orderns leveransmetod. Se [Konfigurera inställningar för Uppfyllt av](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: Välj att ta bort listan från [!DNL Amazon Marketplace]. Se [Avsluta en Amazon-lista](./end-listings-manually.md).

>[!NOTE]
>
>Om du har pågående listor visas antalet listor i ett meddelande ovanför flikarna.

![Aktiva listor](assets/amazon-active-listings.png)

Amazon hemsidor för försäljningskanaler delar några vanliga sidor [arbetsytekontroller](./workspace-controls.md) som gör att du kan anpassa de data som visas.

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | SKU (Stock Keeping Unit) som Amazon har tilldelat en produkt för att identifiera produkt, alternativ, pris och tillverkare. |
| [!UICONTROL ASIN] | Ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt. <br><br>ASIN står för [!DNL Amazon Standard Identification Number]. Ett ASIN är ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt. För böcker är ASIN samma som ISBN-numret, men för alla andra produkter skapas ett nytt ASIN när objektet överförs till deras katalog. Du hittar ett ASIN-objekt på produktinformationssidan på Amazon, tillsammans med mer information om artikeln. |
| [!UICONTROL Product Listing Name] | Produktens namn. |
| [!UICONTROL Condition] | The [villkor](./product-listing-condition.md) av produkten. |
| [!UICONTROL Landed Price] | Produktens listpris plus dess fraktpris. |
| [!UICONTROL Amazon Quantity] | Kvantiteten som är tillgänglig efter att produkten har listats aktivt på Amazon. |
| [!UICONTROL Status] | Status för listan, definierad av Amazon. |
| [!UICONTROL Buy Box Won] | Om produktlistan vann [Buy Box](./buy-box-competitor-pricing.md) position. |
| [!UICONTROL Action] | Lista över tillgängliga åtgärder som kan tillämpas på en viss lista. Om du vill använda en åtgärd klickar du på **[!UICONTROL Select]** i _[!UICONTROL Action]_kolumn för att visa dina alternativ:<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
