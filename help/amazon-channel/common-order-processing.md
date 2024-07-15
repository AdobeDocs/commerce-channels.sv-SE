---
title: Vanliga Amazon-åtgärder för orderbehandling
description: Använd motsvarande  [!DNL Commerce] order som skapats för Amazon-order för att hantera orderaktivitet och bearbetning i [!UICONTROL Commerce] Admin.
feature: Sales Channels, Orders
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Vanliga Amazon-åtgärder för orderbehandling

[Beställningsbehandling för Commerce](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) kan hantera dina Amazon-beställningar, inklusive e-post till köparen, orderhantering (frakt), utfärdande av krediter/återbetalningar, lägga till kommentarer med mera. Om du vill hantera dina Amazon-beställningar måste inställningen [**Importera Amazon-beställningar**](./order-settings.md) vara `Enabled` så att motsvarande [!DNL Commerce]-beställningar skapas när Amazon-beställningar tas emot. Beställningsinformationen för Amazon visas i avsnittet *[!UICONTROL Recent Orders]* på kontrollpanelen för butiker.

När det här alternativet är aktiverat skapas motsvarande [!DNL Commerce] order för Amazon-order och Amazon-ordernumret visas i kolumnen _[!UICONTROL Order Number]_. Om en motsvarande [!DNL Commerce]-order skapas klickar du på ordernumret för att öppna ordern på sidan [Commerce orderbearbetning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). Du kan hantera beställningen på samma sätt som du gör din andra [[!DNL Commerce] beställningsbearbetning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order).

[!DNL Commerce]-ordernumret visas inte med _[!UICONTROL Recent Orders]_-informationen. Beställningsnumret för Commerce visas bara när du klickar på ordernumret på butikens kontrollpanel och öppnar ordern i [Commerce orderbearbetning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order). När beställningen [!DNL Commerce] visas visas Amazon-beställningsnumret i avsnittet *[!UICONTROL Payment & Shipping Method]*. Det innehåller även alternativ för *[!UICONTROL View or Cancel Amazon Order]*och *[!UICONTROL View all Amazon Orders]*, beroende på orderns leveransstatus.

Se [Avbryt en ej levererad order](./cancel-unshipped-order.md).

![Amazon beställningsinformation i Commerce-beställningen](assets/amazon-order-number-payment-info.png){width="500"}

När en Amazon-order bearbetas uppdateras och synkroniseras orderinformationen med ditt [!DNL Amazon Seller Central]-konto. Dina kreditinställningar avgör hur ofta beställningsinformation synkroniseras mellan Amazon och Amazon försäljningskanal.

Vanliga [åtgärder för beställningsbearbetning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order) i Commerce är:

- [Beställa åtgärder](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#actions)
- [Beställningssökning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html#order-search)
- [Bearbeta en beställning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order)
   - [Visa en beställning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#view-an-order)
   - [Bearbeta en beställning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#process-an-order)
   - [Beställnings- och kontoinformation](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-and-account-information)
   - [Adressinformation](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#address-information)
   - [Betalnings- och leveranssätt](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#payment--shipping-method)
   - [Granska beställda objekt](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#review-items-ordered)
- [Utfärdar kredit/återbetalning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/credit-memos/credit-memo-create.html)
- [Uppfyll/leverera en beställning](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/shipments.html#create-a-shipment)
- [Skapa en faktura](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/invoices.html#create-an-invoice)
- [Avbryt en ej levererad order](./cancel-unshipped-order.md)

>[!NOTE]
>
>Om en beställning har statusen `Unshipped` kan du [avbryta en Amazon-beställning](./cancel-unshipped-order.md) på sidan [[!UICONTROL Amazon Order Details]](./amazon-order-details.md). Om en order har skickats kan den inte annulleras.

Se [Commerce Order Management](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/introduction.html#order-management-and-operations).
