---
title: Hantera Amazon-beställningar
description: Du kan aktivera orderimport i orderinställningarna för att enklare hantera dina Amazon-beställningar från Commerce Admin.
feature: Sales Channels, Orders
exl-id: 018a8936-2f03-4a2d-b9af-6b72729ca709
source-git-commit: 7fff4c463551089fb64f2d5bf7bf23f272ce4663
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# Hantera Amazon-beställningar

Du kan visa din beställningsinformation för Amazon, som du fått från Amazon, i avsnittet _[!UICONTROL Recent Orders]_på [butikspanelen](./amazon-store-dashboard.md) eller på sidan_[!UICONTROL Amazon orders]_ (kallas även _[!UICONTROL All Orders]_-vyn).

Hur du hanterar dina Amazon-beställningar beror på om orderimporten är aktiverad eller inaktiverad i [orderinställningarna](./order-settings.md#configure-order-settings).

## Med orderimport aktiverad

Efter [butiksintegrering](./store-integration.md) är [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings)-inställningen `Enabled` som standard. Med den här inställningen skapas motsvarande [!DNL Commerce] order för dina Amazon-beställningar och kan hanteras i arbetsflödet [[!DNL Commerce] Beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).

>[!NOTE]
>
>Oavsett inställningarna för orderimport importeras inte Amazon-beställningar som fanns på ditt [!DNL Amazon Seller Central]-konto innan [butiksintegreringen](./store-integration.md).

Importerade Amazon-order hanteras i arbetsflödet [[!DNL Commerce] Beställningar](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html), precis som dina andra [!DNL Commerce]-butiker. Klicka på Amazon ordernummer i kolumnen *[!UICONTROL Order Number]* för att öppna ordern i [[!DNL Commerce] orderprocessen](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/order-processing.html#process-an-order#order-view-descriptions). Se [Visa Amazon-beställningar](./amazon-orders-all.md).

### Beställningsimportprocess

När en beställning placeras på Amazon och [orderimport](./order-settings.md) är aktiverat börjar följande process.

| Ändra | Åtgärder |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| En beställning görs på Amazon. | <ul><li>Amazon anger orderstatusen till `Pending`.</li><li>Orderinformation skickas till [!DNL Commerce].</li><li>Ordern läggs till i [_Amazon-beställningar_-tabellen](./amazon-orders-all.md) med statusen `Pending`.</li></ul> |
| Amazon ändrar orderstatusen till `Unshipped`. | <ul><li>Statusändringen skickas till [!DNL Commerce].</li><li>I [_Amazon-tabellen_ order](./amazon-orders-all.md) ändras orderstatusen till `Unshipped`.</li><li>I [[!DNL Commerce] orderarbetsflödet](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) skapas en motsvarande [!DNL Commerce]-ordning med statusen `Processing`.</li></ul> |
| I [[!DNL Commerce] orderarbetsflöde](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html) bearbetas [!DNL Commerce]-ordningen och statusen ändras till `Shipped`. | <ul><li>I [_Amazon-tabellen_ order](./amazon-orders-all.md) ändras orderstatusen till `Shipped`.</li><li>På nästa cron-jobb ändras orderstatusen till `Complete` i [[!DNL Commerce] orderarbetsflödet](https://experienceleague.adobe.com/docs/commerce-admin/stores-sales/order-management/orders/orders.html).</li></ul> |

### Orderspärrar

Det finns några scenarier som förhindrar att motsvarande [!DNL Commerce]-ordning skapas. [!DNL Commerce] order skapas inte för order som tas emot när någon av följande problem inträffar.

| Scenario | Lösning |
|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Objektet finns inte i katalogen [!DNL Commerce]. | [Skapa produkten](./creating-assigning-catalog-products.md) i din [!DNL Commerce]-katalog och [matcha den ](./creating-assigning-catalog-products.md) manuellt med produkten. |
| Objektet i katalogen är inaktiverat. | Kontrollera att [produktstatus](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) är aktiverad. |
| Den beställda artikeln är inte i lager. | Uppdatera eller konfigurera [produktalternativen](https://experienceleague.adobe.com/docs/commerce-admin/inventory/configuration/product-options.html) för kvantitet och källa. |

När det inte går att importera beställningar visas ett systemmeddelande som liknar följande längst upp på skärmen:

`Your Amazon store(s) has orders that cannot be imported into [!DNL Commerce]. See Recent Orders in the store dashboard(s): <store name>`

När problemet är löst skapas ordningen [!DNL Commerce] vid nästa synkronisering.

## Beställningsimporten är inaktiverad

Om du inte vill importera och hantera dina Amazon-beställningar i [!DNL Commerce] kan du ändra inställningen [**[!UICONTROL Import Amazon Orders]**](./order-settings.md#configure-order-settings) till `Disabled`. Den här inställningen innebär att när nya order tas emot från Amazon skapas inga motsvarande [!DNL Commerce] order.

När detta är inaktiverat visas orderinformation som tas emot från Amazon i avsnittet _[!UICONTROL Recent Orders]_på kontrollpanelen för butiker och i vyn_[!UICONTROL All Orders]_. Orderinformationen är endast synlig och du måste hantera beställningarna i [!DNL Amazon Seller Central]. Om du vill öppna orderinformationen i [!DNL Amazon Seller Central] klickar du på Amazon-ordernumret i kolumnen _[!UICONTROL Order Number]_.

Se även [Visa Amazon-beställningar](./amazon-orders-all.md), [Visa Amazon-beställningsinformation](./amazon-order-details.md) och [Vanliga beställningsbehandlingar](./common-order-processing.md).
