---
title: Vanliga Amazon-åtgärder för orderbehandling
description: Använd motsvarande [!DNL Commerce] order som skapats för Amazon beställningar för att hantera orderaktivitet och -bearbetning i [!UICONTROL Commerce] Admin.
feature: Sales Channels, Orders
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '476'
ht-degree: 0%

---

# Vanliga Amazon-åtgärder för orderbehandling

[Bearbetning av handelsorder](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) kan hantera dina Amazon-beställningar, inklusive skicka e-post till köparen, utföra beställningen (frakten), utfärda krediter/återbetalningar, lägga till kommentarer och mycket annat. För att hantera dina Amazon-beställningar [**Importera Amazon-beställningar**](./order-settings.md) inställningen måste anges till `Enabled` så att motsvarande [!DNL Commerce] beställningar skapas när Amazon-beställningar tas emot. Amazon beställningsinformation finns i *[!UICONTROL Recent Orders]* -avsnittet på butikspanelen.

När det är aktiverat, motsvarar [!DNL Commerce] beställningar skapas för Amazon och Amazon ordernummer visas i _[!UICONTROL Order Number]_kolumn. Om en motsvarande [!DNL Commerce] ordern skapas, klicka på ordernumret för att öppna ordern i [Bearbetning av handelsorder](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) sida. Du kan hantera beställningen precis som du gör med andra [[!DNL Commerce] orderhantering](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

The [!DNL Commerce] ordernumret visas inte med _[!UICONTROL Recent Orders]_information. Handelsordernumret visas bara när du klickar på ordernumret på butikens kontrollpanel och öppnar ordern i [Bearbetning av handelsorder](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). När du visar [!DNL Commerce] beställningen visas Amazon ordernummer i *[!UICONTROL Payment & Shipping Method]*-avsnitt. Den innehåller även alternativ för att *[!UICONTROL View or Cancel Amazon Order]*och *[!UICONTROL View all Amazon Orders]*, beroende på orderns leveransstatus.

Se [avbryta en ej levererad order](./cancel-unshipped-order.md).

![Amazon orderinformation i handelsorder](assets/amazon-order-number-payment-info.png){width="500"}

När en Amazon-beställning bearbetas uppdateras och synkroniseras beställningsinformationen med din [!DNL Amazon Seller Central] konto. Dina kreditinställningar avgör hur ofta beställningsinformation synkroniseras mellan Amazon och Amazon försäljningskanal.

Common Commerce [orderhantering](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) uppgifter:

- [Orderåtgärder](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [Ordningssökning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [Bearbeta en beställning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [Visa en order](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [Bearbeta en beställning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [Beställnings- och kontoinformation](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [Adressinformation](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [Betalnings- och leveranssätt](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [Granska beställda artiklar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [Utfärda kredit/återbetalning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [Fylla i/leverera en order](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [Skapa en faktura](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [Avbryt en ej levererad order](./cancel-unshipped-order.md)

>[!NOTE]
>
>Om en order finns `Unshipped` status kan du [avbryta en Amazon-beställning](./cancel-unshipped-order.md) på [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) sida. Om en order har skickats kan den inte annulleras.

Se [Hantering av handelsorder](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
