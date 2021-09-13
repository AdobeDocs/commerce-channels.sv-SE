---
title: Vanliga orderbearbetningsuppgifter
description: Använd motsvarande [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] administratör.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Vanliga åtgärder för orderbehandling

[[!DNL Commerce] Beställningsbehandling](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} kan hantera dina Amazon-beställningar, t.ex. skicka e-post till köparen, utföra beställningen (frakt), utfärda krediter/återbetalningar, lägga till kommentarer med mera. Om du vill hantera dina Amazon-beställningar måste inställningen [**Importera Amazon-beställningar**](./order-settings.md) vara `Enabled` så att motsvarande [!DNL Commerce]-beställningar skapas när Amazon-beställningar tas emot. Beställningsinformationen för Amazon visas i avsnittet *[!UICONTROL Recent Orders]* på butikspanelen.

När det här alternativet är aktiverat skapas motsvarande [!DNL Commerce]-order för Amazon-order och Amazon-ordernumret visas i kolumnen _[!UICONTROL Order Number]_. Om en motsvarande [!DNL Commerce]-ordning skapas klickar du på ordernumret för att öppna ordern på sidan [!DNL Commerce] [orderbearbetning](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. Du kan hantera ordningen på samma sätt som du gör andra [[!DNL Commerce] orderbearbetningar](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

Ordernumret [!DNL Commerce] visas inte med _[!UICONTROL Recent Orders]_-informationen. Ordernumret [!DNL Commerce] visas bara när du klickar på ordernumret på butikens kontrollpanel och öppnar ordern i [[!DNL Commerce] orderbearbetningen](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. När du visar ordningen [!DNL Commerce] visas Amazon ordernummer i avsnittet *[!UICONTROL Payment & Shipping Method]*. Den innehåller även alternativ för *[!UICONTROL View or Cancel Amazon Order]*och *[!UICONTROL View all Amazon Orders]*, beroende på orderns leveransstatus.

Se [avbryt en ej levererad order](./cancel-unshipped-order.md).

![Amazon orderinformation i handelsorder](assets/amazon-order-number-payment-info.png)

När en Amazon-order bearbetas uppdateras och synkroniseras orderinformationen med ditt [!DNL Amazon Seller Central]-konto. Dina kreditinställningar avgör hur ofta beställningsinformation synkroniseras mellan Amazon och Amazon försäljningskanal.

Vanliga [!DNL Commerce] [åtgärder för orderbearbetning](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} är:

- [Ordningsåtgärder](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [Ordningssökning](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [Bearbeta en beställning](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [Visa en beställning](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [Bearbeta en beställning](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [Order- och kontoinformation](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [Adressinformation](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [Betalnings- och leveransmetod](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [Granska beställda](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered) objekt {target=&quot;_blank&quot;}
- [Utfärdar kredit/återbetalning](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [Uppfyll/leverera en order](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [Skapa en faktura](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [Avbryt en ej levererad order](./cancel-unshipped-order.md)

>[!NOTE]
>
>Om en order har statusen `Unshipped` kan du [avbryta en Amazon-order](./cancel-unshipped-order.md) på sidan [[!UICONTROL Amazon Order Details]](./amazon-order-details.md). Om en order har skickats kan den inte annulleras.

Se [Hantering av handelsorder](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}.
