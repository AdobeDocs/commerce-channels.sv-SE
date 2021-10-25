---
title: Vanliga orderbearbetningsuppgifter
description: Använd motsvarande [!DNL Commerce] orders created for Amazon orders to manage order activity and processing in the [!UICONTROL Commerce] Admin.
exl-id: a44f36f0-db18-4de5-9c5b-cc68f4793008
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '425'
ht-degree: 0%

---

# Vanliga åtgärder för orderbehandling

[[!DNL Commerce] orderhantering](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} kan hantera dina Amazon-beställningar, inklusive skicka e-post till köparen, genomföra beställningen (frakt), utfärda krediter/återbetalningar, lägga till kommentarer med mera. För att hantera dina Amazon-beställningar [**Importera Amazon-beställningar**](./order-settings.md) inställningen måste anges till `Enabled` så att motsvarande [!DNL Commerce] beställningar skapas när Amazon-beställningar tas emot. Amazon beställningsinformation finns i *[!UICONTROL Recent Orders]* -avsnittet på butikspanelen.

När det är aktiverat, motsvarar [!DNL Commerce] beställningar skapas för Amazon och Amazon ordernummer visas i _[!UICONTROL Order Number]_kolumn. Om en motsvarande [!DNL Commerce] ordern skapas, klicka på ordernumret för att öppna ordern i [!DNL Commerce] [orderhantering](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} sida. Du kan hantera beställningen precis som du gör med andra [[!DNL Commerce] orderhantering](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}.

The [!DNL Commerce] ordernumret visas inte med _[!UICONTROL Recent Orders]_information. The [!DNL Commerce] ordernumret visas bara när du klickar på ordernumret på butikens kontrollpanel och öppnar ordern i [[!DNL Commerce] orderhantering](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}. När du visar [!DNL Commerce] beställningen visas Amazon ordernummer i *[!UICONTROL Payment & Shipping Method]*-avsnitt. Den innehåller även alternativ för att *[!UICONTROL View or Cancel Amazon Order]*och *[!UICONTROL View all Amazon Orders]*, beroende på orderns leveransstatus.

Se [avbryta en ej levererad order](./cancel-unshipped-order.md).

![Amazon orderinformation i handelsorder](assets/amazon-order-number-payment-info.png)

När en Amazon-beställning bearbetas uppdateras och synkroniseras beställningsinformationen med din [!DNL Amazon Seller Central] konto. Dina kreditinställningar avgör hur ofta beställningsinformation synkroniseras mellan Amazon och Amazon försäljningskanal.

Vanliga [!DNL Commerce] [orderhantering](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;} uppgifter:

- [Orderåtgärder](https://docs.magento.com/user-guide/sales/order-actions.html){target=&quot;_blank&quot;}
- [Ordningssökning](https://docs.magento.com/user-guide/sales/orders-search.html){target=&quot;_blank&quot;}
- [Bearbeta en beställning](https://docs.magento.com/user-guide/sales/order-processing.html){target=&quot;_blank&quot;}
   - [Visa en order](https://docs.magento.com/user-guide/sales/order-processing.html#view-an-order){target=&quot;_blank&quot;}
   - [Bearbeta en beställning](https://docs.magento.com/user-guide/sales/order-processing.html#process-an-order){target=&quot;_blank&quot;}
   - [Beställnings- och kontoinformation](https://docs.magento.com/user-guide/sales/order-processing.html#order-and-account-information){target=&quot;_blank&quot;}
   - [Adressinformation](https://docs.magento.com/user-guide/sales/order-processing.html#address-information){target=&quot;_blank&quot;}
   - [Betalnings- och leveranssätt](https://docs.magento.com/user-guide/sales/order-processing.html#payment--shipping-method){target=&quot;_blank&quot;}
   - [Granska beställda artiklar](https://docs.magento.com/user-guide/sales/order-processing.html#review-items-ordered){target=&quot;_blank&quot;}
- [Utfärda kredit/återbetalning](https://docs.magento.com/user-guide/sales/credit-memo-create.html){target=&quot;_blank&quot;}
- [Fylla i/leverera en order](https://docs.magento.com/user-guide/sales/shipments-create.html){target=&quot;_blank&quot;}
- [Skapa en faktura](https://docs.magento.com/user-guide/sales/invoice-create.html){target=&quot;_blank&quot;}
- [Avbryt en ej levererad order](./cancel-unshipped-order.md)

>[!NOTE]
>
>Om en order finns `Unshipped` status kan du [avbryta en Amazon-beställning](./cancel-unshipped-order.md) på [[!UICONTROL Amazon Order Details]](./amazon-order-details.md) sida. Om en order har skickats kan den inte annulleras.

Se [Hantering av handelsorder](https://docs.magento.com/user-guide/sales/order-management.html){target=&quot;_blank&quot;}.
