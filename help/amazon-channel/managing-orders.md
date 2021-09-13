---
title: Hantera order
description: Du kan aktivera orderimport i dina orderinställningar för att enklare hantera dina Amazon-beställningar från din Commerce Admin.
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 2c753ec5f6f4cd509e61b4875e09e9a1a2577ee7
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# Hantera order

Du kan visa din beställningsinformation för Amazon, som du fått från Amazon, i _[!UICONTROL Recent Orders]_-avsnittet på [butikspanelen](./amazon-store-dashboard.md) eller på_[!UICONTROL Amazon orders]_-sidan (kallas även _[!UICONTROL All Orders]_-vyn).

Hur du hanterar dina Amazon-beställningar beror på om orderimporten är aktiverad eller inaktiverad i [orderinställningarna](./order-settings.md#configure-order-settings).

## Med orderimport aktiverad

Efter [butiksintegrering](./store-integration.md) är [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings)-inställningen `Enabled` som standard. Med den här inställningen skapas motsvarande [!DNL Commerce]-order för dina Amazon-order och kan hanteras i arbetsflödet [[!DNL Commerce] Beställningar](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}.

>[!NOTE]
>
>Oavsett inställningarna för orderimport importeras inte Amazon-beställningar som fanns i ditt [!DNL Amazon Seller Central]-konto före din [butiksintegrering](./store-integration.md).

Importerade Amazon-order hanteras i arbetsflödet [[!DNL Commerce] Beställningar](https://docs.magento.com/user-guide/sales/orders.html){target=&quot;_blank&quot;}, precis som dina andra [!DNL Commerce]-butiker. Klicka på Amazon ordernummer i kolumnen *[!UICONTROL Order Number]* för att öppna ordern i [[!DNL Commerce] orderprocessen](https://docs.magento.com/user-guide/sales/order-processing.html#order-view-descriptions){target=&quot;_blank&quot;}. Se [Visa Amazon-beställningar](./amazon-orders-all.md).

### Beställningsimportprocess

När en beställning placeras på Amazon och [orderimport](./order-settings.md) är aktiverat börjar följande process.

| Ändra | Åtgärder |
|---|---|
| En beställning görs på Amazon. | <ul><li>Amazon ställer in orderstatusen på `Pending`.</li><li>Orderinformation skickas till [!DNL Commerce].</li><li>Ordern läggs till i tabellen [_Amazon order_](./amazon-orders-all.md) med statusen `Pending`.</li></ul> |
| Amazon ändrar orderstatusen till `Unshipped`. | <ul><li>Statusändringen skickas till [!DNL Commerce].</li><li>I tabellen [_Amazon order_](./amazon-orders-all.md) ändras orderstatusen till `Unshipped`.</li><li>I [[!DNL Commerce] orderarbetsflödet](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;} skapas en motsvarande [!DNL Commerce]-ordning med statusen `Processing`.</li></ul> |
| I [[!DNL Commerce] orderarbetsflöde](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;} bearbetas ordningen [!DNL Commerce] och statusen ändras till `Shipped`. | <ul><li>I tabellen [_Amazon order_](./amazon-orders-all.md) ändras orderstatusen till `Shipped`.</li><li>På nästa cron-jobb ändras orderstatusen till `Complete` i [[!DNL Commerce] orderarbetsflödet](https://docs.magento.com/user-guide/sales/orders.html){:target=&quot;_blank&quot;}.</li></ul> |

### Orderspärrar

Det finns några scenarier som förhindrar att motsvarande [!DNL Commerce]-ordning skapas. [!DNL Commerce] beställningar skapas inte för beställningar som tas emot när någon av följande utleveranser inträffar.

| Scenario | Lösning |
|---|---|
| Objektet finns inte i [!DNL Commerce]-katalogen. | [Skapa ](./creating-assigning-catalog-products.md) produktionen i din  [!DNL Commerce] katalog och anpassa den  [manuellt ](./creating-assigning-catalog-products.md) efter produkten. |
| Objektet i katalogen är inaktiverat. | Kontrollera att [produktstatus](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;} är aktiverad. |
| Den beställda artikeln är inte i lager. | Uppdatera eller konfigurera [produktalternativen](https://docs.magento.com/user-guide/catalog/inventory-product-stock-options.html){:target=&quot;_blank&quot;} för kvantitet och källa. |

När det inte går att importera beställningar visas ett systemmeddelande som liknar följande längst upp på skärmen:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

När problemet är löst skapas ordningen [!DNL Commerce] vid nästa synkronisering.

## Beställningsimporten är inaktiverad

Om du inte vill importera och hantera dina Amazon-beställningar i [!DNL Commerce] kan du ändra inställningen [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) till `Disabled`. Den här inställningen innebär att när nya order tas emot från Amazon skapas inga motsvarande [!DNL Commerce]-order.

När detta är inaktiverat visas orderinformation som tas emot från Amazon i _[!UICONTROL Recent Orders]_-avsnittet på butikens kontrollpanel och i_[!UICONTROL All Orders]_-vyn. Orderinformationen är endast synlig och du måste hantera beställningarna i [!DNL Amazon Seller Central]. Om du vill öppna orderinformationen i [!DNL Amazon Seller Central] klickar du på Amazon ordernummer i kolumnen _[!UICONTROL Order Number]_.

Se även [Visa Amazon-beställningar](./amazon-orders-all.md), [Visa Amazon-beställningsinformation](./amazon-order-details.md) och [Vanliga beställningsbehandlingar](./common-order-processing.md).
