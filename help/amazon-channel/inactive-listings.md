---
title: Inaktiva listor
description: Amazon försäljningskanal har fliken [!UICONTROL Inactive] för att övervaka dina inaktiva [!DNL Amazon Marketplace] listor.
exl-id: 1d20e75f-3346-48cb-83f7-a9e7acb26a96
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# Inaktiva listor

På fliken _[!UICONTROL Inactive]_visas produkter som har publicerats till Amazon men som inte är aktiva på [!DNL Amazon Marketplace]. Listorna kan vara inaktiva av olika anledningar. Du kanske inte är berättigad att lista just det varumärket. Inaktiva listor styrs av Amazon liststandarder och dina [!DNL Amazon Seller Central]-kontobehörigheter.

Under _[!UICONTROL Actions]_:

- **[!UICONTROL End Listing(s) on Amazon]**: Välj att ta bort alla markerade listor från  [!DNL Amazon Marketplace]. Se [Avsluta en Amazon-lista](./end-listings-manually.md).

- **[!UICONTROL Edit Listing Overrides]**: Välj om du vill ändra åsidosättningsinställningarna för listan. Se [Åsidosätter](./overrides.md) eller [Redigera eller ta bort en åsidosättning](./creating-editing-overrides.md#edit-override-single-listing).

Under **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_:

- **[!UICONTROL View Details]**: Välj om du vill visa listinformation, inklusive  [listningsaktivitetsloggen](./product-listing-details.md#listing-activity-log),  [Buy Boxens konkurrentpriser](./product-listing-details.md#buy-box-competitor-pricing) och  [lägsta konkurrentpriser](./product-listing-details.md#lowest-competitor-pricing). Den här åtgärden är endast avsedd för visning. Inga ändringar kan göras i listinformationen. Se [Visa detaljer](./product-listing-details.md).

- **[!UICONTROL Create Override]**: Välj om du vill skapa en åsidosättning och använda den i den här listan. Se [Skapa en åsidosättning](./creating-editing-overrides.md).

- **[!UICONTROL Edit Assigned ASIN]**: Välj om du vill ändra det ASIN som tilldelats katalogprodukten. Den här åtgärden används om en produkt i din katalog matchades med fel ASIN. Se [Redigera ett tilldelat ASIN](./edit-assigned-asin.md).

- **[!UICONTROL Create Alias Seller SKU]**: Välj om du vill skapa en Alias SKU (stock Keeping unit) som kan användas för att skapa en Amazon-lista från samma katalogprodukt. Se [Skapa en SKU för Aliasförsäljare](./create-alias-seller-sku.md).

- **[!UICONTROL Switch to Fulfilled by Amazon/Merchant]**: Välj om du vill ändra orderns leveransmetod. Se [Konfigurera inställningar som har uppfyllts](./fulfilled-by.md#configure-fulfilled-by-settings).

- **[!UICONTROL End Listing]**: Välj att ta bort listan från  [!DNL Amazon Marketplace]. Se [Avsluta en Amazon-lista](./end-listings-manually.md).

>[!NOTE]
>
>Om du har pågående listor visas ett meddelande ovanför flikarna som anger antalet listor.

![Inaktiva Amazon-listor](assets/amazon-inactive-listings.png)

Amazon hemsidor för försäljningskanaler har gemensamma [kontroller för arbetsytan](./workspace-controls.md) som gör att du kan anpassa de data som visas.

| Kolumn | Beskrivning |
|--- |--- |
| [!UICONTROL Amazon Seller SKU] | SKU (Stock Keeping Unit) som Amazon har tilldelat en produkt för att identifiera produkt, alternativ, pris och tillverkare. |
| [!UICONTROL ASIN] | Ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt.<br><br>ASIN står för Amazon Standard Identification Numbers. Ett ASIN är ett unikt block med 10 bokstäver och/eller siffror som identifierar objekt. För böcker är ASIN samma som ISBN-numret, men för alla andra produkter skapas ett nytt ASIN när objektet överförs till deras katalog. Du hittar ett ASIN-objekt på produktinformationssidan på Amazon, tillsammans med mer information om artikeln. |
| [!UICONTROL Product Listing Name] | Produktens namn. |
| [!UICONTROL Condition] | Produktens [villkor](./product-listing-condition.md). |
| [!UICONTROL Landed Price] | Produktens listpris plus dess fraktpris. |
| [!UICONTROL Amazon Quantity] | Kvantiteten som är tillgänglig när produkten är aktivt listad på Amazon. |
| [!UICONTROL Status] | Status för listan, definierad av Amazon. |
| [!UICONTROL Inactive Reason (if provided by Amazon)] | Amazon ger inte alltid någon anledning till inaktiva listor och ni kan kontakta kundsupport för att lösa listproblem. I vissa fall meddelar Amazon dig om en anledning. Om du vill visa svaren klickar du på **[!UICONTROL View Details]** i kolumnen _[!UICONTROL Action]_. Om dessa problem är åtgärdade och Amazon tar bort felet flyttas produkterna till fliken_[!UICONTROL Active]_. |
| Åtgärd | Lista över tillgängliga åtgärder som kan tillämpas på en viss lista. Om du vill använda en åtgärd klickar du på **[!UICONTROL Select]** i kolumnen _[!UICONTROL Action]_och väljer alternativet:<ul><li>[[!UICONTROL View Details]](./product-listing-details.md)</li><li>[[!UICONTROL Create Override]](./creating-editing-overrides.md)</li><li>[[!UICONTROL Edit Assigned ASIN]](./edit-assigned-asin.md)</li><li>[[!UICONTROL Create Alias Seller SKU]](./create-alias-seller-sku.md#region-specific)</li><li>[[!UICONTROL Switch to Fulfilled By Amazon/Merchant]](./fulfilled-by.md#configure-fulfilled-by-settings)</li><li>[[!UICONTROL End Listing]](./end-listings-manually.md)</li></ul> |
